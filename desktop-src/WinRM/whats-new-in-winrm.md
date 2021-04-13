---
title: Neues in WinRM 2,0
description: In Windows-Remoteverwaltung Version 2,0 sind neue Features verfügbar. (WinRM 2,0).
ms.assetid: 402c179a-6dd7-4d75-9318-bb8194b5527d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54f4a4829bffdb816854de2a3ebe98106a5a65af
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389966"
---
# <a name="whats-new-in-winrm-20"></a>Neues in WinRM 2,0

In Windows-Remoteverwaltung Version 2,0 sind neue Features verfügbar. (WinRM 2,0)

WinRM 2,0 ist in Windows Server 2008 R2 und Windows 7 enthalten.

Sie können auch WinRM 2,0 für Windows Server 2008 mit Service Pack 2 (SP2) und Windows Vista mit Service Pack 2 (SP2) herunterladen. Weitere Informationen zum Herunterladen von WinRM 2,0 finden Sie unter [KB968929](https://support.microsoft.com/kb/968929).

In der folgenden Tabelle ist die Dokumentation für WinRM 2,0 aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="client-shell-api.md">WinRM Client-Shell-API</a><br/></td>
<td>Die WinRM-ClientShell-API (Application Programming Interface) bietet Funktionen zum Erstellen und Verwalten von Shells und shellvorgängen, Befehlen und Datenströmen auf Remote Computern. <br/></td>
</tr>
<tr class="even">
<td><a href="winrm-plugin-api.md">WinRM-Plugin-API</a><br/></td>
<td>Die WinRM-Plug-in-API bietet Funktionen, mit deren Hilfe ein Benutzer Plug-ins schreiben kann, indem er bestimmte APIs für unterstützte <a href="windows-remote-management-glossary.md"><em>Ressourcen-URIs</em></a> und-Vorgänge implementiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="winrm-application-hosting.md">Infrastruktur zum Verwalten von gehosteten Diensten</a><br/></td>
<td>WinRM 2,0 führt ein hostingframework ein. Zwei Hostingmodelle werden unterstützt. Eine davon ist Internet Information Service (IIS) – basiert, die andere ist WinRM – Service based. <br/> Weitere Informationen zur Host Konfiguration finden Sie in den folgenden Themen:<br/>
<ul>
<li><a href="iis-host-plug-in-configuration.md">IIS-Host-Plug-in-Konfiguration</a></li>
<li><a href="wsman-service-plug-in-configuration.md">Konfiguration des WinRM-Dienst-Plug-ins</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="dmtf-association-traversal.md">Ermittlung von DMTF-Profilen durch Zuordnungs Durchlauf</a><br/></td>
<td>Der Zuordnungs Durchlauf ermöglicht einem Benutzer das Abrufen von Instanzen von Zuordnungs Klassen mithilfe eines Standardfilter Mechanismus.<br/></td>
</tr>
<tr class="odd">
<td><a href="remote-shell-infrastructure-improvements.md">Verbesserungen der Remoteshell</a><br/></td>
<td>Dieses Thema enthält Informationen zu den Verbesserungen bei der Remote Infrastruktur von WinRM. <br/></td>
</tr>
<tr class="even">
<td><a href="multi-hop-support.md">Unterstützung für mehrere Hops</a><br/></td>
<td>Die Funktionalität wurde WinRM 2,0 hinzugefügt, die die Delegierung von Benutzer Anmelde Informationen über mehrere Remote Computer unterstützt. <br/> Das Thema <a href="authentication-constants.md"><strong>Authentifizierungs Konstanten</strong></a> wurde aktualisiert, um die folgende Konstante hinzuzufügen: <strong>wsmanflagusecredssp</strong>.<br/> Die folgende C++-API wurde hinzugefügt, um Multi-Hop-Unterstützung bereitzustellen: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.<br/> Die folgende Skript-API wurde hinzugefügt, um Unterstützung für mehrere Hops bereitzustellen: <a href="wsman-sessionflagusecredssp.md"><strong>WSMAN. sessionflagusecredssp</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="quotas.md">Kontingent Verwaltung für Remote Shells</a><br/></td>
<td>Dieses Thema enthält Informationen zur Kontingent Konfiguration für die remoteshellverwaltung.<br/></td>
</tr>
<tr class="even">
<td><a href="winrm-powershell-commandlets.md">Verwaltete Referenz für WS-Management PowerShell-Befehle</a><br/></td>
<td>Benutzer von WinRM 2,0 können Windows PowerShell-Cmdlets für die Systemverwaltung verwenden.<br/></td>
</tr>
</tbody>
</table>



 

 

 





