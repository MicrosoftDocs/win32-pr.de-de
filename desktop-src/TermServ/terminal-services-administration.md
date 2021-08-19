---
title: Remotedesktopdienste Verwaltung
description: Mit Remotedesktopdienste-API können Sie Remotedesktop-Sitzungshost (RD-Sitzungshost), Clientsitzungen und Prozesse aufzählen und verwalten.
ms.assetid: 85a9ed9d-79d6-4011-93a4-00847c689747
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46df6277b924d25608b3c4def5074c1f156738e23d114de075af01521953e7d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000280"
---
# <a name="remote-desktop-services-administration"></a>Remotedesktopdienste Verwaltung

Mit Remotedesktopdienste-API können Sie Remotedesktop-Sitzungshost (RD-Sitzungshost), Clientsitzungen und Prozesse aufzählen und verwalten.

Rufen Sie zum Abrufen der Namen aller RD-Sitzungshost Server in einer Domäne die [**NetServerEnum-Funktion**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) auf, um Server vom Typ SV \_ TYPE \_ TERMINALSERVER aufzählen. Um ein Handle für einen bestimmten RD-Sitzungshost zu öffnen, übergeben Sie den Servernamen in einem Aufruf der [**WTSOpenServer-Funktion.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera) Wenn Sie die Verwendung des Handles abgeschlossen haben, geben Sie es frei, indem Sie die [**WTSCloseServer-Funktion**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver) aufrufen.

Sie können das von **WTSOpenServer zurückgegebene** Handle verwenden, um die folgenden Vorgänge auf dem Server durchzuführen.



| Funktion                                                         | Vorgang                                                                                                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)             | Trennt den Client von einer angegebenen Sitzung. Die Sitzung bleibt aktiv, und der Benutzer kann sich erneut anmelden, um eine Verbindung mit derselben Sitzung herzustellen.                                                                         |
| [**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)             | Gibt eine Liste der Sitzungen auf dem angegebenen RD-Sitzungshost zurück.                                                                                                                                               |
| [**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)           | Gibt eine Liste der Prozesse auf dem angegebenen RD-Sitzungshost zurück.                                                                                                                                              |
| [**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)                     | Meldet die angegebene Sitzung ab.                                                                                                                                                                                   |
| [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) | Gibt Informationen über die angegebene Sitzung auf dem angegebenen RD-Sitzungshost zurück.                                                                                                                          |
| [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)                         | Zeigt ein Meldungsfeld auf der Clientanzeige einer angegebenen Sitzung an.                                                                                                                                                 |
| [**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)                   | Fährt einen angegebenen Server herunter und startet RD-Sitzungshost neu.                                                                                                                                            |
| [**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)               | Beendet einen angegebenen Prozess auf einem angegebenen RD-Sitzungshost Server.                                                                                                                                             |
| [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)           | Öffnet ein Handle für das Serverende eines angegebenen virtuellen Kanals. Weitere Informationen zu virtuellen Kanälen finden Sie unter [Using Remotedesktopdienste Virtual Channels](using-terminal-services-virtual-channels.md). |
| [**Wtswaitsystemevent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)                 | Wartet auf ein Ereignis, z. B. die Erstellung einer Clientsitzung oder eines Benutzers, der sich beim RD-Sitzungshost anmelden.                                                                                                  |



 

Mehrere dieser Funktionen weisen Puffer zu, um Informationen an den Aufrufer zurückgibt. Wenn Sie die Verwendung des Puffers abgeschlossen haben, geben Sie ihn frei, indem Sie die [**WTSFreeMemory-Funktion**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory) aufrufen.

 

 