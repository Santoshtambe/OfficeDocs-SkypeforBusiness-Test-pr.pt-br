﻿---
title: Get-CsVoiceConfiguration
TOCTitle: Get-CsVoiceConfiguration
ms:assetid: c5e7afa3-28d3-4bf9-a2f2-c34932c9a3cd
ms:mtpsurl: https://technet.microsoft.com/pt-br/library/Gg398815(v=OCS.15)
ms:contentKeyID: 49308065
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Get-CsVoiceConfiguration

 

_**Tópico modificado em:** 2015-03-09_

Retrieves the voice configuration object, which contains a full list of all voice test configurations defined for the Lync Server deployment. Este cmdlet foi introduzido no Lync Server 2010.

## Sintaxe

    Get-CsVoiceConfiguration [-Identity <XdsIdentity>] <COMMON PARAMETERS>

    Get-CsVoiceConfiguration [-Filter <String>] <COMMON PARAMETERS>

    COMMON PARAMETERS: [-LocalStore <SwitchParameter>]

## Examples

## EXAMPLE 1

This example retrieves the voice configuration. To retrieve the voice test configurations, use the **Get-CsVoiceTestConfiguration** cmdlet.

    Get-CsVoiceConfiguration

## Detailed Description

Voice test configurations are used to test a phone number against a specific voice policy, route, and dial plan. This cmdlet is used to retrieve the global instance that holds a list of all voice test configurations defined within the Lync Server deployment. To retrieve individual voice test configurations or to retrieve them as individual objects rather than as a list, use the **Get-CsVoiceTestConfiguration** cmdlet.

Who can run this cmdlet: By default, members of the following groups are authorized to run the **Get-CsVoiceConfiguration** cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins. To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

Get-CsAdminRole | Where-Object {$\_.Cmdlets –match "Get-CsVoiceConfiguration"}

## Parâmetros


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>Required</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Filter</em></p></td>
<td><p>Optional</p></td>
<td><p>System.String</p></td>
<td><p>There can only be one instance of this object, so this parameter does nothing.</p></td>
</tr>
<tr class="even">
<td><p><em>Identity</em></p></td>
<td><p>Optional</p></td>
<td><p>Microsoft.Rtc.Management.Xds.XdsIdentity</p></td>
<td><p>The scope of the voice configuration to retrieve. The only possible value is Global.</p></td>
</tr>
<tr class="odd">
<td><p><em>LocalStore</em></p></td>
<td><p>Optional</p></td>
<td><p>System.Management.Automation.SwitchParameter</p></td>
<td><p>Retrieves the voice configuration from the local replica of the Repositório de Gerenciamento Central, rather than the Repositório de Gerenciamento Central itself.</p></td>
</tr>
</tbody>
</table>


## Input Types

None.

## Return Types

This cmdlet returns an instance of the Microsoft.Rtc.Management.WritableConfig.Policy.Voice.VoiceConfiguration object.

## Consulte Também

#### Outros Recursos

[Remove-CsVoiceConfiguration](remove-csvoiceconfiguration.md)  
[Set-CsVoiceConfiguration](set-csvoiceconfiguration.md)  
[Get-CsVoiceTestConfiguration](get-csvoicetestconfiguration.md)

