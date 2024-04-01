# Description
This project is a simple example of gPRC mock server.  
It allows to override responses from real server with custom ones, what is useful for testing.  

# Requirements
* Windows 10 or later
* Visual Studio Community or higher
* vcpkg ([guide](https://vcpkg.io/en/getting-started.html))
* original gPRC-server protobuf profo-files

# Tutorial
* Clone the project using `git clone`
* Copy the `CMakePresets_template.json` file to `CMakePresets.json`
* Change all placeholders with `<TODO: your path>` to your actual paths
* Open the project using Visual Studio (File -> Open -> CMake...)
* Build the project
* Choose the `grpc_mock_server_example.exe` target
* TODO: add responses data
* Ensure that your original gRPC server is accessible (turn on VPN, for example)
* Run the server

# Update the SSL certificate
Execute the command
```
echo quit | openssl s_client -showcerts -servername google.ru -connect google.ru:443 > cacert.pem
```
and then select the first certificate from `cacert.pem`
