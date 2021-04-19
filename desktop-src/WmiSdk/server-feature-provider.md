---
description: Ab Windows Server 2008 liefert der Server Funktions Anbieter Informationen dazu, welche Server Funktionen auf dem Server installiert sind. Mit dieser Klasse können Administratoren ihre Server Rollen und Features inventarisieren und verwalten.
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: Server Funktions Anbieter
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350271"
---
# <a name="server-feature-provider"></a>Server Funktions Anbieter

Ab Windows Server 2008 liefert der Server Funktions Anbieter Informationen dazu, welche Server Funktionen auf dem Server installiert sind. Mit dieser Klasse können Administratoren ihre Server Rollen und Features inventarisieren und verwalten.

Eine Server Rolle ist als eine Gruppe von Komponenten definiert, die Funktionen für einen bestimmten Funktionsbereich bereitstellen, z. b. Drucken, Dateien, Domänen Steuerung usw. Typische Server Rollen sind Dateiserver, e-Mail-Server, DNS-Server, Domänen Controller, Anwendungsserver usw.

Wenn in einem Unternehmen keine Verwaltungssoftware ausgeführt wird, die Server Rollen meldet (z. b. Microsoft Operations Manager mit installierten Management Packs), können Sie diese Informationen abrufen, indem Sie die Win32-Klasse " [**\_ Serverfeature**](win32-serverfeature.md) " Abfragen. Server Rollen-und Featureinformationen von Remote Computern sind über normale WMI-Remote Verbindungen oder mithilfe des Windows-Remoteverwaltung-Dienstanbieter (WinRM) verfügbar. Weitere Informationen zu Remote-WMI-DCOM-Verbindungen finden [Sie unter Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md). Weitere Informationen zu Verbindungen mit dem [*WS-Verwaltungs*](/windows/desktop/WinRM/windows-remote-management-glossary) Protokoll finden Sie unter [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal).

Der Server Funktions Anbieter unterstützt die folgenden WMI-Klassen:

-   [**Win32- \_ Server Funktion**](win32-serverfeature.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Anbieter](wmi-providers.md)
</dt> </dl>

 

 
