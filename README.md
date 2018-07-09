AGS-component-http-request
==========================

> AGS components are a set of AutoIt libraries, that you can use in your AutoIt project build with the [AGS framework](https://v20100v.github.io/autoit-gui-skeleton/). AGS-component-http-request is a library used to send HTTP request in POST or GET method in an AutoIt project build with AGS framework.


<br/>

## Description

### Methods

This library provides few method to handle HTTP request.

 Methods    | Description 
---------------|-------------
`HttpGET($url, $data = "", $proxy = "")` | Send HTTP request with GET method.
`HttpPOST($url, $data = "", $proxy = "")` | Send HTTP request with POST method.
`URLEncode($urlText)` | URL encoding replaces unsafe ASCII characters.  
`URLDecode($urlText)` | Inverse operation of URLEncode.
`WinHttp_SetProxy_from_configuration_file($oHttp)` | Set timeouts by parsing the configuration file AGS project store in './config/parameters.ini'.
`WinHttp_SetProxy_from_configuration_file($oHttp)` | Set proxy by parsing the configuration file AGS project store in './config/parameters.ini'.


### Usages

#### Make a simple HTTP request in GET

```autoit
#include 'vendor/ags-component-http-request/ags-component-http-request.au3'

;=====================================================================================
; Func HttpGET($url, $data = "", $proxy = "")
; @param $url (string)    : URL want to open
; @param $data (string)   : Data to be posted by GET method (?param1=23&param2=ibicf)
; @param $proxy (string)  : Specify a proxy. By default we load proxy settings form 
;                           configuration file - ./config/parameters.ini
; @return $oHttp (object) : Instance of the Winhttprequest.5.1 object
;=====================================================================================

Local $response = HttpGET( _ 
    "https://soundcloud.com/2080/my-megadrive", _ 
    default, _ 
    "http://myproxy.com:20100")
    
ConsoleWrite($response.Status & @CRLF)
ConsoleWrite($response.ResponseText)
```
 

<br/>

## Configure and install it

### Requirements 

To install this AGS component, we use [Yarn](https://yarnpkg.com/en/docs/install#windows-stable) as a package manager for AutoIt code of AGS framework. We divert the orignal use of Yarn, a tool in Node.js ecosystm use to handle Javascript module. We assume that you already install `Node.js` and `Yarn`, and if it's not the case, we suggest you to take a [chocolatey](https://chocolatey.org/), in ordre to install them. Chocolatey is THE package manager for Windows. It easily manage all aspects of Windows software (installation, configuration, upgrade, and uninstallation). 

In order to install `Node.js` and `Yarn` just run your prefered windows command ; cmd, cmder or powershell ; as an administrator and type:

```bash
λ choco install nodejs
λ choco install yarn
```

And to install `AGS-component-http-request`, just type in the root folder of your project ; i.e. where the `package.json` of your project is store.

```
λ yarn install ags-component-http-request
```

    
<br/>
 
## Dependencies
  
> Specifiy if this AGS component have dependencies with an third-party library AutoIt or with an anoter AGS component. 
  
 - AutoIt library dependencies : none.
 - AGS-components dependencies : none.
  
 
<br/>
 
## About
 
### Release history
 
 - ags-component-http-request v1.0.0-alpha - *2018.07.09*
 
### Contributing
 
Comments, pull-request & stars are always welcome !
 
### License
 
Copyright (c) 2018 by [v20100v](https://github.com/v20100v). Released under the MIT license.