gluster-rest
============

A server providing a RESTful web api for access to the Gluster management
daemon.

Presently it is just a quick hack written in go, which given the gluster cli
arguments with a '/' as the seperator, runs the gluster cli with the arguments
and returns the xml output. There is no input validation or proper error
reporting as yet, but these will come soon.

The GoRest framework [1] is used to build the server.

To install and test, run `# go get github.com/kshlm/gluster-rest`  
This will download, compile and install gluster-rest and GoRest in your
`$GOPATH`.

Run `$GOPATH/bin/gluster-rest` as root, to start the server.  
The base URI for requests will be `http://localhost:7331/gluster`

To get the list of volumes, you can do a GET request on
`http://localhost:7331/gluster/volume/list`  
This will return an xml document containing the list of volumes in the cluster.

To get information regarding a volume do a GET request on
`http://localhost:7331/gluster/volume/info/<VOLUMENAME>`  
This will return an xml document containing information on the given volume.

[1]: https://code.google.com/p/gorest/ "GoRest"
