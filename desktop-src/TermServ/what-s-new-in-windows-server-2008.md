---
title: Neues in Windows Server 2008
description: Windows Server 2008 führt die folgenden neuen Programmier Elemente für Terminal Dienste ein.
ms.assetid: a2299b03-5e06-4984-a33f-b44c7cded513
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab74f22c41fa88147a1ef30a8f55f158e34990c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104391118"
---
# <a name="whats-new-in-windows-server-2008"></a>Neues in Windows Server 2008

Windows Server 2008 führt die folgenden neuen Programmier Elemente für Terminal Dienste ein.



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
<td>Mit den APIs für dynamische virtuelle Kanäle (DVC) werden die vorhandenen virtuellen Channel-APIs für Terminal Dienste erweitert, die als statische virtuelle Channel-APIs bezeichnet werden.<br/>
<ul>
<li><a href="dynamic-virtual-channels.md">Dynamische virtuelle Kanäle</a></li>
<li><a href="dynamic-virtual-channels-reference.md">Referenz zu dynamischen virtuellen Kanälen</a></li>
</ul></td>
</tr>
<tr class="even">
<td>Remotedesktop-Webverbindung Referenz<br/></td>
<td>Die folgenden Schnittstellen (und die zugehörigen Methoden und Eigenschaften) wurden <a href="remote-desktop-web-connection-reference.md">Remotedesktop-Webverbindung Verweis</a>hinzugefügt:<br/>
<ul>
<li><a href="imsrdpclient5.md"><strong>IMsRdpClient5-Schnittstelle</strong></a></li>
<li><a href="imsrdpclient6.md"><strong>IMsRdpClient6-Schnittstelle</strong></a></li>
<li><a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5-Schnittstelle</strong></a></li>
<li><a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6-Schnittstelle</strong></a></li>
<li><a href="imsrdpclientnonscriptable3.md"><strong>IMsRdpClientNonScriptable3-Schnittstelle</strong></a></li>
<li><a href="imsrdpclientshell.md"><strong>Imsrdpclientshell-Schnittstelle</strong></a></li>
<li><a href="imsrdpclienttransportsettings.md"><strong>Imsrdpclienttransportsettings-Schnittstelle</strong></a></li>
<li><a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2-Schnittstelle</strong></a></li>
<li><a href="imsrdpdevice.md"><strong>Imsrdpdevice-Schnittstelle</strong></a></li>
<li><a href="imsrdpdevicecollection.md"><strong>Imsrdpdebug-Schnittstelle</strong></a></li>
<li><a href="imsrdpdrive.md"><strong>Imsrdpdrive-Schnittstelle</strong></a></li>
<li><a href="imsrdpdrivecollection.md"><strong>Imsrdpdrivecollection-Schnittstelle</strong></a></li>
<li><a href="itsremoteprogram.md"><strong>Itsremoteprogram-Schnittstelle</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Referenz zur terminaldiensteapi<br/></td>
<td>Die folgenden Funktionen wurden der <a href="terminal-services-api-reference.md">Referenz zur terminaldiensteapi</a>hinzugefügt:<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona"><strong>Wzconneczession-Funktion</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex"><strong>Wzregistersessionnotificationex-Funktion</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona"><strong>Wout startremotecontrolsession-Funktion</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession"><strong>Wout stopremotecontrolsession-Funktion</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex"><strong>Wtsunregistersessionnotificationex-Funktion</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex"><strong>Wout virtualchannelopenex-Funktion</strong></a></li>
</ul>
Die folgenden Strukturen wurden hinzugefügt:<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta"><strong>WTSClient-Struktur</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa"><strong>Wtsinfo-Struktur</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Terminal Dienste-WMI-Anbieter<br/></td>
<td>Die folgenden Klassen und Methoden wurden dem <a href="terminal-services-wmi-provider.md">Terminal Dienste-WMI-Anbieter</a>hinzugefügt.<br/>
<ul>
<li><a href="terminal-services-gateway-classes.md">Terminaldienstegateway-Klassen (und zugeordnete Methoden)</a></li>
<li><a href="terminal-services-license-server-classes.md">Terminal Dienste-Lizenz Server Klassen (und zugehörige Methoden)</a></li>
<li><a href="terminal-services-remoteapp-classes.md">RemoteApp-Klassen (und zugeordnete Methoden)</a></li>
<li><a href="win32-tsdiscoveredlicenseserver.md"><strong>Win32_TSDiscoveredLicenseServer-Klasse</strong></a></li>
<li><a href="create-win32-terminal.md"><strong>Create-Methode der Win32_Terminal-Klasse</strong></a></li>
<li><a href="delete-win32-terminal.md"><strong>Delete-Methode der Win32_Terminal-Klasse</strong></a></li>
<li><a href="canaccesslicenseserver-win32-terminalservicesetting.md"><strong>Canaccesslicenseserver-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="findlicenseservers-win32-terminalservicesetting.md"><strong>Findlicenseservers-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="getdomain-win32-terminalservicesetting.md"><strong>GetDomain-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="getgraceperioddays-win32-terminalservicesetting.md"><strong>Getgraceperioddays-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="getwinstationdrivernames-win32-terminalservicesetting.md"><strong>Getwinstationdrivernames-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="pinglicenseserver-win32-terminalservicesetting.md"><strong>Pinglicenseserver-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="updatedirectconnectlicenseserver-win32-terminalservicesetting.md"><strong>Updatedirectconnectlicenseserver-Methode der Win32_TerminalServiceSetting-Klasse</strong></a></li>
<li><a href="setuserauthenticationrequired-win32-tsgeneralsetting.md"><strong>Setuserauthenticationrequired-Methode der Win32_TSGeneralSetting-Klasse</strong></a></li>
<li><a href="getcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Getcurrentredirectableadressen-Methode der Win32_TSSessionDirectory-Klasse</strong></a></li>
<li><a href="setcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Setcurrentredirectableadressen-Methode der Win32_TSSessionDirectory-Klasse</strong></a></li>
<li><a href="getredirectableaddresses-win32-tssessiondirectory.md"><strong>Getredirectableadressen-Methode der Win32_TSSessionDirectory-Klasse</strong></a></li>
<li><a href="pingsessiondirectory-win32-tssessiondirectory.md"><strong>Pingsessiondirectory-Methode der Win32_TSSessionDirectory-Klasse</strong></a></li>
<li><a href="setloadbalancingstate-win32-tssessiondirectory.md"><strong>Setloadbalancingstate-Methode der Win32_TSSessionDirectory-Klasse</strong></a></li>
<li><a href="setserverweight-win32-tssessiondirectory.md"><strong>Setserverweight-Methode der Win32_TSSessionDirectory-Klasse</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Plug-in-Referenz zum Terminal Dienste-Sitzungs Broker<br/></td>
<td>Das Terminal Dienste-Sitzungs Broker-Plug-in wird verwendet, um die Funktionen des Terminal Dienste-Sitzungs Brokers zu erweitern.<br/>
<ul>
<li><a href="/windows/desktop/TermServ/terminal-services-virtualization-api-reference">Plug-in-Referenz zum Terminal Dienste-Sitzungs Broker</a></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

