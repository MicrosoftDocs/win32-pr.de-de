---
title: RAS-Server-Sicherheits Authentifizierung
description: Wenn ein Windows NT/Windows 2000-RAS-Server einen Aufruf empfängt, ruft er die Funktion "rassecuritydialogbegin" der registrierten RAS-Sicherheits-DLL auf, sofern vorhanden.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27184388b418e0fec2a1988fd9e693e942c08e03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036870"
---
# <a name="ras-server-security-authentication"></a>RAS-Server-Sicherheits Authentifizierung

Wenn ein Windows NT/Windows 2000-RAS-Server einen Aufruf empfängt, ruft er die Funktion " [**rassecuritydialogbegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) " der registrierten RAS-Sicherheits-DLL auf, sofern vorhanden. Mit diesem Befehl wird die Sicherheits-DLL benachrichtigt, damit die Authentifizierung des Remote Benutzers gestartet wird. Der RAS-Server ruft vor seiner PPP-oder RAS-Authentifizierung " **rassecuritydialogbegin** " auf.

Der Befehl " [**rassecuritydialogbegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) " übergibt die folgenden Informationen an die Sicherheits-DLL:

-   Ein Port handle, mit dem die Verbindung identifiziert werden soll.
-   Zeiger auf Puffer, die bei der Kommunikation mit dem Remote Benutzer verwendet werden sollen.
-   Ein Zeiger auf eine " [**rassecuritydialogcomplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) "-Funktion, die aufgerufen wird, wenn die Authentifizierung abgeschlossen ist.

Das Port Handle und die Puffer Zeiger sind gültig, bis die Sicherheits-dll " [**rassecuritydialogcomplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) " aufruft, um die Authentifizierungs Transaktion zu beenden.

Mit der Datei " [**rassecuritydialogcomplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) " wird der RAS-Server über die Ergebnisse der Authentifizierung der Sicherheits-DLL des Remote Benutzers benachrichtigt. Wenn die Sicherheits-DLL einen Erfolg meldet, fährt der RAS-Server mit der PPP-und RAS-Authentifizierung des Remote Benutzers fort. Wenn die Sicherheits-DLL meldet, dass der Remote Benutzer die Authentifizierung nicht bestanden hat, oder wenn ein Fehler aufgetreten ist, wird der RAS-Server beendet und protokolliert den Fehler oder die Authentifizierung im Ereignisprotokoll.

 

 




