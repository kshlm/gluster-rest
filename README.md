gluster-rest
============

A server providing a RESTful web api for access to the Gluster management
daemon.

Presently it is just a quick hack written in go, which given the gluster cli
arguments with a '/' as the seperator, runs the gluster cli with the arguments
and returns the xml output. There is no input validation or proper error
reporting as yet, but these will come soon.

To install and test, run
        # go install github.com/kshlm/gluster-rest

This will download, compile and install gluster-rest and dependencies in your
$GOPATH

