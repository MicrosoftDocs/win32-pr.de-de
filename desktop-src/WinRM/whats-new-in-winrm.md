---
title: Neuerungen in WinRM 2.0
description: Neue Features sind in Windows Version 2.0 der Remoteverwaltung verfügbar. (WinRM 2.0).
ms.assetid: 402c179a-6dd7-4d75-9318-bb8194b5527d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d322b0b86600cd783bd787427b53df334f3d499a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480586"
---
# <a name="whats-new-in-winrm-20"></a>Neuerungen in WinRM 2.0

Neue Features sind in Windows Version 2.0 der Remoteverwaltung verfügbar. (WinRM 2.0)

WinRM 2.0 ist in Windows Server 2008 R2 und Windows 7 enthalten.

Sie können auch WinRM 2.0 für Windows Server 2008 mit Service Pack 2 (SP2) und Windows Vista mit Service Pack 2 (SP2) herunterladen. Informationen zum Herunterladen von WinRM 2.0 finden Sie unter [KB968929.](https://support.microsoft.com/kb/968929)

In der folgenden Tabelle ist die Dokumentation für WinRM 2.0 aufgeführt.




| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="client-shell-api.md">WinRM Client-Shell-API</a><br /> | Die WinRM Client Shell-API (Application Programming Interface) bietet Funktionen zum Erstellen und Verwalten von Shells und Shellvorgängen, Befehlen und Datenströmen auf Remotecomputern. <br /> | 
| <a href="winrm-plugin-api.md">WinRM-Plug-In-API</a><br /> | Die WinRM-Plug-In-API bietet Funktionen, mit denen Benutzer Plug-Ins schreiben können, indem bestimmte APIs für unterstützte <a href="windows-remote-management-glossary.md"><em>Ressourcen-URIs</em></a> und -Vorgänge implementiert werden.<br /> | 
| <a href="winrm-application-hosting.md">Infrastruktur zum Verwalten gehosteter Dienste</a><br /> | WinRM 2.0 führt ein Hostingframework ein. Zwei Hostingmodelle werden unterstützt. Eine ist iis-basiert (Internetinformationsdienst) und die andere winRM-dienstbasiert. <br /> Weitere Informationen zur Hostkonfiguration finden Sie in den folgenden Themen:<br /><ul><li><a href="iis-host-plug-in-configuration.md">Konfiguration des IIS-Host-Plug-Ins</a></li><li><a href="wsman-service-plug-in-configuration.md">WinRM-Dienst-Plug-In-Konfiguration</a></li></ul> | 
| <a href="dmtf-association-traversal.md">DMTF-Profilermittlung durch Zuordnungsdurchlauf</a><br /> | Der Zuordnungsdurchlauf ermöglicht einem Benutzer das Abrufen von Instanzen von Zuordnungsklassen mithilfe eines Standardfiltermechanismus.<br /> | 
| <a href="remote-shell-infrastructure-improvements.md">Verbesserungen der RemoteShell-Infrastruktur</a><br /> | Dieses Thema enthält Informationen zu den Verbesserungen der Remoteinfrastruktur für WinRM. <br /> | 
| <a href="multi-hop-support.md">Unterstützung für mehrere Hops</a><br /> | Die Funktionalität wurde zu WinRM 2.0 hinzugefügt, die das Delegieren von Benutzeranmeldeinformationen über mehrere Remotecomputer hinweg unterstützt. <br /> Das Thema <a href="authentication-constants.md"><strong>Authentifizierungskonstanten</strong></a> wurde aktualisiert, um die folgende Konstante hinzuzufügen: <strong>WSManFlagUseCredSsp.</strong><br /> Die folgende C++-API wurde hinzugefügt, um Unterstützung für mehrere Hops bereitzustellen: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.<br /> Die folgende Skript-API wurde hinzugefügt, um Unterstützung für mehrere Hops bereitzustellen: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan.SessionFlagUseCredSsp.</strong></a><br /> | 
| <a href="quotas.md">Kontingentverwaltung für Remoteshells</a><br /> | Dieses Thema enthält Informationen zur Kontingentkonfiguration für die Remoteshellverwaltung.<br /> | 
| <a href="winrm-powershell-commandlets.md">Verwaltete Referenz für WS-Management PowerShell-Befehle</a><br /> | Benutzer von WinRM 2.0 können Windows PowerShell Cmdlets für die Systemverwaltung verwenden.<br /> | 




 

 

 





