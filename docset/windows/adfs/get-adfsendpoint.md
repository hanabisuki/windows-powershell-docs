---
ms.mktglfcycl: manage
ms.sitesec: library
ms.author: brianlic
author: brianlic-msft-msft
description: Use this topic to help manage Windows and Windows Server technologies with Windows PowerShell.
external help file: Microsoft.IdentityServer.Management.dll-Help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 2016-12-20
ms.prod: w10
ms.technology: powershell-windows
ms.topic: reference
online version: 
schema: 2.0.0
title: Get-AdfsEndpoint
ms.assetid: 8ECE0D0C-1463-409D-BDE2-4325447FEC46
---

# Get-AdfsEndpoint

## SYNOPSIS
Retrieves an endpoint in AD FS.

## SYNTAX

### Address (Default)
```
Get-AdfsEndpoint [[-AddressPath] <String[]>] [<CommonParameters>]
```

### FullUrl
```
Get-AdfsEndpoint [-FullUrl] <Uri[]> [<CommonParameters>]
```

## DESCRIPTION
The **Get-AdfsEndpoint** cmdlet retrieves a specified endpoint from Active Directory Federation Services (AD FS).
The collection of **AdfsEndpoint** objects is a list of all the supported endpoints that are on the server.
You can use this list to view the configuration of endpoints and enable or disable them.
To see the full list of endpoints, use this cmdlet with no parameters.

## EXAMPLES

### Example 1: Get an endpoint
```
PS C:\> Get-AdfsEndpoint -AddressPath "/adfs/services/trust/13/Windows"
```

This command gets the WS-Trust 1.3 endpoint.

## PARAMETERS

### -AddressPath
Specifies an array of address paths that do not include the AD FS service name.
The cmdlet gets endpoints that correspond to the paths that you specify.
An example of such a path is /adfs/portal/updatepassword.

```yaml
Type: String[]
Parameter Sets: Address
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -FullUrl
Specifies the full URL of the endpoint to retrieve.

```yaml
Type: Uri[]
Parameter Sets: FullUrl
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.IdentityServer.PowerShell.Resources.Endpoint
This cmdlet returns class structure that represents the endpoints for the Federation Service.

## NOTES
* Endpoints provide access to the federation server functionality of AD FS, such as token issuance and the publication of federation metadata. Depending on the type of endpoint, you can enable or disable the endpoint or control whether the endpoint is published to Web Application Proxy.

## RELATED LINKS

[Disable-AdfsEndpoint](./Disable-AdfsEndpoint.md)

[Enable-AdfsEndpoint](./Enable-AdfsEndpoint.md)

[Set-AdfsEndpoint](./Set-AdfsEndpoint.md)
