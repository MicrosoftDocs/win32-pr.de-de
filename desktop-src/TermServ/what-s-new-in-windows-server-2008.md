---
title: Neuerungen in Windows Server 2008
description: Windows Server 2008 führt die folgenden neuen Programmierelemente für Terminaldienste ein.
ms.assetid: a2299b03-5e06-4984-a33f-b44c7cded513
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a13dc35286a38a8164461643bf2b124413b04790877de7ebbc11174ce53894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868600"
---
# <a name="whats-new-in-windows-server-2008"></a>Neuerungen in Windows Server 2008

Windows Server 2008 führt die folgenden neuen Programmierelemente für Terminaldienste ein.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Programmierelement</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Referenz zu dynamischen virtuellen Kanälen<br/></td>
<td>Dynamische APIs für virtuelle Kanäle (DYNAMIC Virtual Channel, DVC) erweitern die vorhandenen APIs für virtuelle Kanäle für Terminaldienste, die als APIs für statische virtuelle Kanäle (Static Virtual Channel, SVC) bezeichnet werden.<br/>
<ul>
<li><a href="dynamic-virtual-channels.md">Dynamische virtuelle Kanäle</a></li>
<li><a href="dynamic-virtual-channels-reference.md">Referenz zu dynamischen virtuellen Kanälen</a></li>
</ul></td>
</tr>
<tr class="even">
<td>Remotedesktop-Webverbindung-Referenz<br/></td>
<td>Die folgenden Schnittstellen (und die zugehörigen Methoden und Eigenschaften) wurden <a href="remote-desktop-web-connection-reference.md">Remotedesktop-Webverbindung Verweis</a>hinzugefügt:<br/>
<ul>
<li><a href="imsrdpclient5.md"><strong>IMsRdpClient5-Schnittstelle</strong></a></li>
<li><a href="imsrdpclient6.md"><strong>IMsRdpClient6-Schnittstelle</strong></a></li>
<li><a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5-Schnittstelle</strong></a></li>
<li><a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6-Schnittstelle</strong></a></li>
<li><a href="imsrdpclientnonscriptable3.md"><strong>IMsRdpClientNonScriptable3-Schnittstelle</strong></a></li>
<li><a href="imsrdpclientshell.md"><strong>IMsRdpClientShell-Schnittstelle</strong></a></li>
<li><a href="imsrdpclienttransportsettings.md"><strong>IMsRdpClientTransportSettings-Schnittstelle</strong></a></li>
<li><a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2-Schnittstelle</strong></a></li>
<li><a href="imsrdpdevice.md"><strong>IMsRdpDevice-Schnittstelle</strong></a></li>
<li><a href="imsrdpdevicecollection.md"><strong>IMsRdpDeviceCollection-Schnittstelle</strong></a></li>
<li><a href="imsrdpdrive.md"><strong>IMsRdpDrive-Schnittstelle</strong></a></li>
<li><a href="imsrdpdrivecollection.md"><strong>IMsRdpDriveCollection-Schnittstelle</strong></a></li>
<li><a href="itsremoteprogram.md"><strong>ITSRemoteProgram-Schnittstelle</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Api-Referenz für Terminaldienste<br/></td>
<td>Die folgenden Funktionen wurden der <a href="terminal-services-api-reference.md">API-Referenz</a>für Terminaldienste hinzugefügt:<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona"><strong>WTSConnectSession-Funktion</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex"><strong>WTSRegisterSessionNotificationEx-Funktion</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona"><strong>WTSStartRemoteControlSession-Funktion</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession"><strong>WTSStopRemoteControlSession-Funktion</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex"><strong>WTSUnRegisterSessionNotificationEx-Funktion</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex"><strong>WTSVirtualChannelOpenEx-Funktion</strong></a></li>
</ul>
Die folgenden Strukturen wurden hinzugefügt:<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta"><strong>WTSCLIENT-Struktur</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa"><strong>WTSINFO-Struktur</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>WMI-Anbieter für Terminaldienste<br/></td>
<td>Die folgenden Klassen und Methoden wurden dem <a href="terminal-services-wmi-provider.md">WMI-Anbieter</a>für Terminaldienste hinzugefügt.<br/>
<ul>
<li><a href="terminal-services-gateway-classes.md">Gatewayklassen für Terminaldienste (und zugeordnete Methoden)</a></li>
<li><a href="terminal-services-license-server-classes.md">Lizenzserverklassen für Terminaldienste (und zugehörige Methoden)</a></li>
<li><a href="terminal-services-remoteapp-classes.md">RemoteApp-Klassen (und zugeordnete Methoden)</a></li>
<li><a href="win32-tsdiscoveredlicenseserver.md"><strong>Win32_TSDiscoveredLicenseServer-Klasse</strong></a></li>
<li><a href="create-win32-terminal.md"><strong>Create-Methode der Win32_Terminal-Klasse</strong></a></li>
<li><a href="delete-win32-terminal.md"><strong>Delete-Methode der Win32_Terminal-Klasse</strong></a></li>
<li><a href="canaccesslicenseserver-win32-terminalservicesetting.md"><strong>CanAccessLicenseServer-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="findlicenseservers-win32-terminalservicesetting.md"><strong>FindLicenseServers-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="getdomain-win32-terminalservicesetting.md"><strong>GetDomain-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="getgraceperioddays-win32-terminalservicesetting.md"><strong>GetGracePeriodDays-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="getwinstationdrivernames-win32-terminalservicesetting.md"><strong>GetWinstationDriverNames-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="pinglicenseserver-win32-terminalservicesetting.md"><strong>PingLicenseServer-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="updatedirectconnectlicenseserver-win32-terminalservicesetting.md"><strong>UpdateDirectConnectLicenseServer-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="setuserauthenticationrequired-win32-tsgeneralsetting.md"><strong>SetUserAuthenticationRequired-Methode der Win32_TSGeneralSetting-Klasse</strong></a></li>
<li><a href="getcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>GetCurrentRedirectableAddresses-Methode der Win32_TSSessionDirectory-Klasse</strong></a></li>
<li><a href="setcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>SetCurrentRedirectableAddresses-Methode der Win32_TSSessionDirectory-Klasse</strong></a></li>
<li><a href="getredirectableaddresses-win32-tssessiondirectory.md"><strong>GetRedirectableAddresses-Methode der Win32_TSSessionDirectory-Klasse</strong></a></li>
<li><a href="pingsessiondirectory-win32-tssessiondirectory.md"><strong>PingSessionDirectory-Methode der Win32_TSSessionDirectory-Klasse</strong></a></li>
<li><a href="setloadbalancingstate-win32-tssessiondirectory.md"><strong>SetLoadBalancingState-Methode der Win32_TSSessionDirectory-Klasse</strong></a></li>
<li><a href="setserverweight-win32-tssessiondirectory.md"><strong>SetServerWeight-Methode der Win32_TSSessionDirectory-Klasse</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Plug-In-Referenz für Terminaldienste-Sitzungsbroker<br/></td>
<td>Das Plug-In Terminal Services Session Broker (TS Session Broker) wird verwendet, um die Funktionen des TS-Sitzungsbrokers zu erweitern.<br/>
<ul>
<li><a href="/windows/desktop/TermServ/terminal-services-virtualization-api-reference">Referenz zum Sitzungsbroker für Terminaldienste</a></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

