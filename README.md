Caching Proxy Server

A simple caching proxy server built with Node.js, Express, and NodeCache. This server forwards requests to an origin server, caches responses, and handles subsequent requests efficiently.

File Structure

Caching Proxy/

│

├── caching-proxy.js       # Main script for the caching proxy server

├── package.json           # Node.js project metadata and dependencies

├── package-lock.json      # Auto-generated file for dependency locking

├── README.md              # Documentation for the project

└── .gitignore             # Specifies files to be ignored by Git

Requirements:

Ensure the following are installed on your system:

Node.js (v14 or later)

Download and install from Node.js Official Website.

npm (Node Package Manager)

Comes bundled with Node.js.

Dependencies


The project requires the following npm packages:


express: For setting up the server.
axios: For making HTTP requests to the origin server.
node-cache: For caching responses.
yargs: For parsing command-line arguments.

Install all dependencies by running:

   npm install

How to Use

1. Clone the Repository
   
Clone the project to your local machine:

git clone <repository-url>

   cd Caching Proxy

2. Install Dependencies
   
Run the following command to install required npm packages:

   npm install

4. Start the Proxy Server
   
Run the server with the required arguments:

   node caching-proxy.js --port <PORT> --origin <ORIGIN_URL>
	
   Replace <PORT> with the port number and <ORIGIN_URL> with the origin server URL.

Example:

node caching-proxy.js --port 8080 --origin http://example.com

4. Clear the Cache

To clear the cache, use the clear-cache command:
node caching-proxy.js clear-cache

Features

Caching: Stores responses from the origin server for subsequent requests.

Command-line Interface: Easily configurable via yargs.

Cache Control: Clear the cache on demand using the clear-cache command.

Redirect Handling: Detects and logs redirects.

Testing


Use tools like curl, Postman, or a browser to test the proxy server:


curl http://localhost:<PORT>/<endpoint>

The first request will return X-Cache: MISS.

Subsequent requests to the same endpoint will return X-Cache: HIT.

Troubleshooting

Common Issues:


Missing Required Arguments: Ensure --port and --origin are provided when starting the server.
Server Not Starting: Check if the port is already in use or if Node.js is installed properly.
No Response: Verify the origin server URL is correct and accessible.


License


MIT License
Copyright (c) 2023 Mithradevi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
