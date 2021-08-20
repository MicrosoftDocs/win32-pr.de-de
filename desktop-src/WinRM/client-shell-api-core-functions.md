---
title: Client Shell API Core Functions
description: Die folgende Tabelle enthält eine Übersicht über die Kernfunktionen für die Clientshell-API Windows Remoteverwaltung (WinRM).
ms.assetid: cd0e6b55-03e8-4ebe-aea8-35d268cdb18c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36a081723af60acf08aa9b4123cc124c2635371bfb50053da457289343ceec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113343"
---
# <a name="client-shell-api-core-functions"></a>Client Shell API Core Functions

Die folgende Tabelle enthält eine Übersicht über die Kernfunktionen für die Clientshell-API Windows Remoteverwaltung (WinRM).



| Core-Funktionen                                                   | Beschreibung                                                                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManCloseCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosecommand)                   | Schließt einen Befehl.                                                                                                                                                               |
| [**WSManCloseOperation**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseoperation)               | Schließt einen Vorgang.                                                                                                                                                            |
| [**WSManCloseSession**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosesession)                   | Schließt eine WinRM-Sitzung.                                                                                                                                                         |
| [**WSManCloseShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseshell)                       | Schließt ein Shellobjekt.                                                                                                                                                          |
| [**WSManConnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshell)                   | Stellt eine Verbindung mit einer vorhandenen Serversitzung her.                                                                                                                                         |
| [**WSManConnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshellcommand)     | Stellt eine Verbindung mit einem vorhandenen Befehl her, der in einer Shell ausgeführt wird.                                                                                                                             |
| [**WSManCreateSession**](/windows/desktop/api/Wsman/nf-wsman-wsmancreatesession)                 | Erstellt eine WinRM-Sitzung.                                                                                                                                                        |
| [**WSManCreateShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell)                     | Erstellt ein Shellobjekt.                                                                                                                                                         |
| [**WSManCreateShellEx**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshellex)                 | Erstellt ein Shellobjekt mit der gleichen Funktionalität wie die [**WSManCreateShell-Funktion,**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) wobei eine vom Client angegebene Shell-ID hinzufügung wird.          |
| [**WSManDeinitialize**](/windows/desktop/api/Wsman/nf-wsman-wsmandeinitialize)                   | Initialisiert den WinRM-Clientstapel.                                                                                                                                           |
| [**WSManDisconnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmandisconnectshell)             | Trennt die Netzwerkverbindung einer aktiven Shell und der zugehörigen Befehle.                                                                                              |
| [**WSManInitialize**](/windows/desktop/api/Wsman/nf-wsman-wsmaninitialize)                       | Initialisiert WinRM.                                                                                                                                                              |
| [**WSManReceiveShellOutput**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput)       | Empfängt die Shellausgabe.                                                                                                                                                          |
| [**WSManReconnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshell)               | Verbindet eine zuvor getrennte Shellsitzung erneut. Verwenden Sie [**WSManReconnectShellCommand,**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand)um die zugeordneten Befehle der Shellsitzung erneut zu verbinden. |
| [**WSManReconnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand) | Verbindet einen zuvor getrennten Befehl erneut.                                                                                                                                   |
| [**WSManRunShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand)             | Führt einen Shellbefehl aus.                                                                                                                                                           |
| [**WSManRunShellCommandEx**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommandex)         | Stellt die gleiche Funktionalität wie die [**WSManRunShellCommand-Funktion**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand) bereit, wobei eine Befehls-ID-Option hinzufügung wird.                                 |
| [**WSManSendShellInput**](/windows/desktop/api/Wsman/nf-wsman-wsmansendshellinput)               | Sendet Eingaben an eine Shell.                                                                                                                                                         |
| [**WSManSignalShell**](/windows/desktop/api/Wsman/nf-wsman-wsmansignalshell)                     | Signalisiert einer Shell.                                                                                                                                                                |



 

 

 




