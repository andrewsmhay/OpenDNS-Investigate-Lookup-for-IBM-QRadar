## Synopsis

This is a simple [OpenDNS Investigate](http://www.opendns.com/enterprise-security/solutions/investigate/) right-click integration for use within [IBM Security QRadar SIEM](http://www-03.ibm.com/software/products/en/qradar-siem) using the built-in <code>ip_context_menu.xml</code> file - located on the QRadar console in the <code>/opt/qradar/conf/</code> directory.

## Installation

1. Clone the repository locally or download the <code>ip_context_menu.xml</code> file.

2. Upload the <code>ip_context_menu.xml</code> file to your QRadar console.

<code>$ **scp ip_context_menu.xml root@*\<QRadar console IP\>*:.**</code>

3. Using SSH, log in to QRadar as the root user:

<code>$ **ssh root@\<QRadar console IP\>**</code>

4. Back up your existing  <code>ip_context_menu.xml</code> file:

<code>$ **mv /opt/qradar/conf/ip_context_menu.xml /opt/qradar/conf/ip_context_menu.xml.orig**</code>

5. Copy your new <code>ip_context_menu.xml</code> file into the configuration directory:

<code>$ **cp ~/ip_context_menu.xml /opt/qradar/conf/ip_context_menu.xml**</code>

*Note: Copy any previous settings from your original <code>ip_context_menu.xml </code> file into this new file, if required.*

6. Restart the tomcat service:

<code># **service tomcat restart**</code>

## Contributors

Andrew Hay, Sr. Security Research Lead and Evangelist, OpenDNS, Inc.

Twitter: [@andrewsmhay](http://twitter.com/andrewsmhay)

## License

Copyright (C) 2014 OpenDNS, Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

IBM, the IBM logo, and ibm.com are trademarks or registered trademarks of International Business Machines Corp., registered in many jurisdictions worldwide. Other product and service names might be trademarks of IBM or other companies. A current list of IBM trademarks is available on the Web at “Copyright and trademark information” at [www.ibm.com/legal/copytrade.shtml](http://www.ibm.com/legal/copytrade.shtml).