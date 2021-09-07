
A super hacky fork of brownie. 

Let me show you its features:

* Brownie test mode now has a --portoverride xxxx command, which allows modification of the RPC's port at cli
  * This allows for externally managed parellel testing (with many RPC clients on one host), with the intent to host on a AWS cluster using RAY.
  * Currently due to hacky nature will only work for default network
* Revert Exceptions can be optionally supressed so they do not cause test failures
  * In my tests some contract calls may revert but I dont care, nor do i know / care what revert is raised - this allows the test to continue.
 
 


## License

This project is licensed under the [MIT license](LICENSE).
