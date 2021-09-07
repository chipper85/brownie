
A super hacky fork of brownie. 

Let me show you its features:

* Brownie test mode now has a --portoverride xxxx command, which allows modification of the RPC's port at cli
  * This allows for externally managed parellel testing (with many RPC clients on one host), with the intent to host on a AWS cluster using RAY.
  * Currently due to hacky nature will only work for default network
  * example: brownie test --portoverride 8666

* Revert Exceptions can be optionally supressed so they do not cause test failures
  * In my tests some contract calls may revert but I dont care, nor do I know / care what revert is raised - this allows the test to continue.
  * example: self.token_under_test.approve(address_0, uint256_0, {'from': caller_address, 'suppress_revert': True})
 


## License

This project is licensed under the [MIT license](LICENSE).
