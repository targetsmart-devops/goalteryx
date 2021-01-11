<img src="https://github.com/tlarsen7572/goalteryx/blob/master/goalteryx_icon_whiteBackground.png?raw=true" width="200">

# GoAlteryx

An unofficial SDK for building custom Alteryx tools with Go.

## Why a Go SDK?

With the announced deprecation of the .NET SDK, a gap formed between the C/C++ and Python SDKs.  C/C++ are low-level languages requiring great care and expertise to ensure proper memory management.  Python is very approachable but is slower.  I wanted to build tools with a middle-ground language having decent performance and simplified memory management.  Go fit the bill and is my favorite language to code in.

## Table of contents

1. [Installation](#Installation)  
2. [Building your custom tools](#Building-your-custom-tools)  
3. [Sample tool](#Sample-tool)  
4. [Registering your tool](#Registering-your-tool)  
5. [Implementing the Plugin interface](#Implementing-the-Plugin-interface)  
6. [Using Provider](#Using-Provider)  
7. [Using OutputAnchor](#Using-OutputAnchor)  
8. [Using Io](#Using-Io)  
9. [Using Environment](#Using-Environment)  
10. [Using InputAnchor](#Using-InputAnchor)  
11. [RecordInfo](#RecordInfo)  
12. [Using RecordPacket](#Using-RecordPacket)  

## Installation

Install goalteryx using Go modules: `go get github.com/tlarsen7572/goalteryx`

## Building your custom tools

You should specify the output DLL file and make sure `-buildmode` is set to `c-shared`.  For reference, the following command is used to build the included example tools:

```
go build -o "C:\Program Files\Alteryx\bin\Plugins\goalteryx.dll" -buildmode=c-shared goalteryx/implementation_example
```

I build directly to the Plugins folder in the Alteryx installation folder of my dev environment.  This allows me to rebuild my tools and run them directly in Alteryx without additional copying.  You do not need to close and restart Alteryx when you rebuild a DLL.  The next time you run a workflow with your custom tool, the new DLL will be used.  It should go without saying that you should not do this in production.

[Back to table of contents](#Table-of-contents)

## Sample tool

[Back to table of contents](#Table-of-contents)

## Registering your tool

[Back to table of contents](#Table-of-contents)

## Implementing the Plugin interface

[Back to table of contents](#Table-of-contents)

## Using Provider

[Back to table of contents](#Table-of-contents)

## Using OutputAnchor

[Back to table of contents](#Table-of-contents)

## Using Io

[Back to table of contents](#Table-of-contents)

## Using Environment

[Back to table of contents](#Table-of-contents)

## Using InputAnchor

[Back to table of contents](#Table-of-contents)

## RecordInfo

[Back to table of contents](#Table-of-contents)

## Using RecordPacket

[Back to table of contents](#Table-of-contents)
