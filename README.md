This project was originally intended to allow creation of full CAdES compliant signatures. I may yet get it into that state.
Along the way, it morphed into something that can be used to interrogate any property or extension of a certificate. Anything beyond the Certificate class and its dependencies hasn't been tested, and probably doesn't work.

The Certificate class has been tested using about 750,000 certificates from various sources, and at least in terms of reading certs, is robust. One implementation of this is the CertToXML project, which runs on Windows, and will take a cert, and emit an XML document with everything in human readable form. This needs Visual Studio to build - I haven't put in the effort to get CMake to also manage this.

The other is the get_crl project, which builds and runs on Linux. It's surprisingly difficult to get openssl to cough up the CRL URLs in a robust way, and this code will do that. This builds correctly with CMake.
