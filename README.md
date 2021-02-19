# Bridge for Codemaster's F1 2019
This bridge is capable of streaming the game's telemetry (PC or Console). It is intended to be run on a pc on your local network.

# Requirements to run the sample
- .Net Core 3.0 SDK https://dotnet.microsoft.com/download/dotnet-core/3.0

# Run the sample
- TODO

# Content of the sample
- Bridge.Codemasters.sln: The solution file describing what projects to include
- Bridge.Codemasters.Console: The console application wiring up the code so it can transform incoming data and send it to quix. This is what you can configure via appsettings.json.
- Bridge.Codemasters.Quix: Contains logic to transform data objects to quix and send it to the platform.
- Bridge.Codemasters: Contains game specific logic for transforming the byte packets to usable data objects.


# Bridge.Codemasters.Console sppsettings.json
The application has two modes of running. 
- "udp": Set "Input" to "udp". This will listen to UDP packages on the network according to the "UDPInput" configuration.
- "file" Set "Input" to "file". This will replay one or more files specified under "FileInput" configuration.
More information can be found in Bridge.Codemasters.Console/Configuration/Config.cs.
