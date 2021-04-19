---
title: Remotedesktopdienste Verwaltung
description: Die Remotedesktopdienste-API ermöglicht es Ihnen, Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server, Client Sitzungen und Prozesse aufzulisten und zu verwalten.
ms.assetid: 85a9ed9d-79d6-4011-93a4-00847c689747
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e763a652335c85931225746334bc21db0e6e086d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341738"
---
# <a name="remote-desktop-services-administration"></a>Remotedesktopdienste Verwaltung

Die Remotedesktopdienste-API ermöglicht es Ihnen, Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server, Client Sitzungen und Prozesse aufzulisten und zu verwalten.

Rufen Sie zum Abrufen der Namen aller RD-Sitzungshost Server in einer Domäne die [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) -Funktion auf, um Server des \_ Typs "Terminalserver" vom Typ "SV Type" aufzulisten \_ . Wenn Sie ein Handle für einen bestimmten RD-Sitzungshost Server öffnen möchten, übergeben Sie den Servernamen in einem aufzurufenden Befehl an die Funktion [**wzopenserver**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera) . Wenn Sie die Verwendung des Handles abgeschlossen haben, geben Sie es durch Aufrufen der [**wtscloseserver**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver) -Funktion frei.

Sie können das von **wzopenserver** zurückgegebene Handle verwenden, um die folgenden Vorgänge auf dem Server auszuführen.



| Funktion                                                         | Vorgang                                                                                                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wzdisconneczession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)             | Trennt den Client von einer angegebenen Sitzung. Die Sitzung bleibt aktiv, und der Benutzer kann sich erneut anmelden, um eine Verbindung mit derselben Sitzung herzustellen.                                                                         |
| [**Wtseneneratesessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)             | Gibt eine Liste der Sitzungen auf dem angegebenen RD-Sitzungshost Server zurück.                                                                                                                                               |
| [**Wtsenum erateprocesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)           | Gibt eine Liste der Prozesse auf dem angegebenen RD-Sitzungshost Server zurück.                                                                                                                                              |
| [**Wunglogoffsession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)                     | Protokolliert die angegebene Sitzung.                                                                                                                                                                                   |
| [**Wzquerysessioninformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) | Gibt Informationen über die angegebene Sitzung auf dem angegebenen RD-Sitzungshost Server zurück.                                                                                                                          |
| [**Wtssendmessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)                         | Zeigt ein Meldungs Feld auf der Client Anzeige einer angegebenen Sitzung an.                                                                                                                                                 |
| [**Wungshutdownsystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)                   | Wird heruntergefahren und optional ein angegebener RD-Sitzungshost Server neu gestartet.                                                                                                                                            |
| [**Wtsterminateprocess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)               | Beendet einen angegebenen Prozess auf einem angegebenen RD-Sitzungshost Server.                                                                                                                                             |
| [**Wout virtualchannelopen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)           | Öffnet ein Handle für das Server Ende eines angegebenen virtuellen Kanals. Weitere Informationen zu virtuellen Kanälen finden Sie unter [Verwenden von Remotedesktopdienste virtuellen Kanälen](using-terminal-services-virtual-channels.md). |
| [**Wout waitsystemevent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)                 | Wartet auf ein Ereignis, z. b. die Erstellung einer Client Sitzung oder eines Benutzers, der sich am RD-Sitzungshost Server anmeldet.                                                                                                  |



 

Einige dieser Funktionen weisen Puffer zu, um Informationen an den Aufrufer zurückzugeben. Wenn Sie die Verwendung des Puffers abgeschlossen haben, können Sie ihn durch Aufrufen der [**wtionfreememory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory) -Funktion freigeben.

 

 