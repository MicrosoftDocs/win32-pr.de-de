---
title: Kernfunktionen der ClientShell-API
description: In der folgenden Tabelle finden Sie eine Übersicht über die wichtigsten Funktionen für die-ClientShell-API von Windows-Remoteverwaltung (WinRM).
ms.assetid: cd0e6b55-03e8-4ebe-aea8-35d268cdb18c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebfe3390b3808cd0abbe9d6bf4ea83ccb0a92338
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388372"
---
# <a name="client-shell-api-core-functions"></a>Kernfunktionen der ClientShell-API

In der folgenden Tabelle finden Sie eine Übersicht über die wichtigsten Funktionen für die-ClientShell-API von Windows-Remoteverwaltung (WinRM).



| Core-Funktionen                                                   | BESCHREIBUNG                                                                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wsmanclosecommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosecommand)                   | Schließt einen Befehl.                                                                                                                                                               |
| [**Wsmancloseoperation**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseoperation)               | Schließt einen Vorgang.                                                                                                                                                            |
| [**Wsmanclosesession**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosesession)                   | Schließt eine WinRM-Sitzung.                                                                                                                                                         |
| [**Wsmancloseshell**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseshell)                       | Schließt ein Shellobjekt.                                                                                                                                                          |
| [**Wsmanconnectshell**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshell)                   | Stellt eine Verbindung mit einer vorhandenen Server Sitzung her.                                                                                                                                         |
| [**Wsmanconnectshellcommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshellcommand)     | Verbindung mit einem vorhandenen Befehl, der in einer Shell ausgeführt wird.                                                                                                                             |
| [**Wsmankreatesession**](/windows/desktop/api/Wsman/nf-wsman-wsmancreatesession)                 | Erstellt eine WinRM-Sitzung.                                                                                                                                                        |
| [**Wsmankreateshell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell)                     | Erstellt ein Shellobjekt.                                                                                                                                                         |
| [**Wsmankreateshellex**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshellex)                 | Erstellt ein Shellobjekt, indem die gleiche Funktionalität wie die [**wsmankreateshell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) -Funktion mit dem Hinzufügen einer vom Client angegebenen shellid verwendet wird.          |
| [**Wsmandeinitialize**](/windows/desktop/api/Wsman/nf-wsman-wsmandeinitialize)                   | Deinitialisiert den WinRM-Client Stapel.                                                                                                                                           |
| [**Wsmandisconnectshell**](/windows/desktop/api/Wsman/nf-wsman-wsmandisconnectshell)             | Trennt die Netzwerkverbindung einer aktiven Shell und der zugehörigen Befehle.                                                                                              |
| [**Wsmaninitialize**](/windows/desktop/api/Wsman/nf-wsman-wsmaninitialize)                       | Initialisiert WinRM.                                                                                                                                                              |
| [**Wsmanreceiveshelloutput**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput)       | Empfängt die shellausgabe.                                                                                                                                                          |
| [**Wsmanreconnectshell**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshell)               | Verbindet eine zuvor getrennte Shellsitzung erneut. Verwenden Sie zum erneuten Verbinden der zugehörigen Befehle der Shellsitzung [**wsmanreconnectshellcommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand). |
| [**Wsmanreconnectshellcommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand) | Verbindet einen zuvor getrennten Befehl erneut.                                                                                                                                   |
| [**Wsmanrunshellcommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand)             | Führt einen Shellbefehl aus.                                                                                                                                                           |
| [**Wsmanrunshellcommandex**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommandex)         | Bietet die gleiche Funktionalität wie die [**wsmanrunshellcommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand) -Funktion, wobei eine Befehls-ID-Option hinzugefügt wird.                                 |
| [**Wsmansendshellinput**](/windows/desktop/api/Wsman/nf-wsman-wsmansendshellinput)               | Sendet Eingaben an eine Shell.                                                                                                                                                         |
| [**Wsmansignalshell**](/windows/desktop/api/Wsman/nf-wsman-wsmansignalshell)                     | Signalisiert eine Shell.                                                                                                                                                                |



 

 

 




