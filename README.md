<!-- [![Build Status](https://travis-ci.org/luongnv89/pcap_dump.svg?branch=master)](https://travis-ci.org/luongnv89/pcap_dump) -->

### Introduce

A simple c/cpp API for processing URI

The list of extensions from [Root Zone Database](http://www.iana.org/domains/root/db)


### API 

```
/**
 * Check the validation of given URI
 * @param  uri URI to check
 * @param  uri_len the length of URI
 * @return     1 - if the given URI is a valid URI
 *               0 - if the given URI is not a valid URI
 *               
 */
int up_valid_uri(char * uri, int uri_len);
```

Check the validation of a given URI

```
/**
 * Get hostname from a given URI
 * @param  uri URI
 * @param  uri The length of URI
 * @return     a pointer points to a new string of the hostname
 *               NULL if the URI is invalid
 */
char * up_get_host(char * uri, int uri_len);
```

Get hostname from a given URI

```
/**
 * Get domain name from a given URI
 * @param  uri     URI
 * @param  uri_len The length of URI
 * @return         a pointer points to a new string of the domainname 
 *               NULL if the URI is invalid
 */
char * up_get_domain(char * uri, int uri_len);
```

Get domain name from a given URI

```
/**
 * Get subdomain name from a given URI
 * @param  uri     URI
 * @param  uri_len length of URI
 * @return         a pointer points to a new string of the subdomain
 *                 NULL:
 *                 	- URI is invalid
 *                 	- There is no subdomain
 */	
char * up_get_subdomain(char * uri, int uri_len); 
```

Get subdomain name from a given URI

### Install

No need to install it. Just include this file in your code and use the API.  

```
#include "uri_proc.h"
```

Compile your program:

```
gcc -o mytest uri_proc/uri_proc.c mytest.c
```

You can look at the example to see how it works.

### Change logs

- 24/04/2017: Create APIs list