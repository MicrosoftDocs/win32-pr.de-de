---
description: Dienstanbieter implementieren detaillierte Telefoniegerätesteuerungen. Ein Telefoniedienstanbieter (Telefoniedienstanbieter, TSP) stellt Anrufsteuerungen bereit, und ein Mediendienstanbieter stellt, sofern vorhanden, die Kontrolle über den Medienstream bereit.
ms.assetid: eb63d55e-4a2b-4bc0-8001-99772f418d72
title: Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0bc427b79daadc8dc89e49a29e18ebbd9797bed74da7f890dc851d6ee97b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773120"
---
# <a name="service-providers"></a>Dienstanbieter

Dienstanbieter implementieren detaillierte Telefoniegerätesteuerungen. Ein Telefoniedienstanbieter (Telefoniedienstanbieter, TSP) stellt Anrufsteuerungen bereit, und ein Mediendienstanbieter stellt, sofern vorhanden, die Kontrolle über den Medienstream bereit.

Alle Telefoniedienstanbieter werden im TAPISRV-Prozess ausgeführt. Dienstanbieter können Threads im TAPISRV-Kontext nach Bedarf erstellen, um ihre Arbeit zu erledigen, und sicher sein, dass keine der erstellten Ressourcen durch das Beenden einer einzelnen Anwendung zerstört wird. Der TAPI-Server übersetzt Anwendungsbefehle nach Bedarf in einen konsistenten Satz von Befehlen, die als Telefoniedienstanbieterschnittstelle (Telefoniedienstanbieterschnittstelle, TSPI) bezeichnet werden.

Mediendienstanbieter werden im Prozessbereich der Anwendung ausgeführt, sodass die schnelle Antwort in Mediensteuerelementen manchmal erforderlich ist. Die TAPI-DLL ermöglicht die konsistente Einhaltung der Media Service Provider Interface (MSPI).

Ausführlichere Informationen zu den Dienstanbietern finden Sie unter [Übersicht über TAPI-Dienstanbieter.](./tapi-service-provider-overview.md)

Unterhalb der Telefoniedienstanbieter-DLL kann der Dienstanbieter beliebige Systemfunktionen oder andere erforderliche Komponenten verwenden. Zu diesen Funktionen gehören [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) und [**DeviceIoControl,**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)die mit unabhängigen Kernelmoduskomponenten und -diensten des Hardwareanbieters sowie mit Standardgeräten wie seriellen und parallelen Anschlüssen zusammenarbeiten, um externe, lokal angeschlossene Geräte zu steuern. Sie können auch auf Netzwerkdienste (z. B. RPC, Windows Sockets und Named Pipes) für client-/serverseitige Telefonie zugreifen.

Die Benutzeroberfläche des Telefoniedienstanbieters wird von TAPI in den Prozess einer Anwendung geladen, die eine der Dienstanbieterfunktionen aufruft, die ein Dialogfeld anzeigen können (z. B. [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)). Der Dienstanbieter kann auch dazu führen, dass seine zugeordnete UI-DLL geladen und im Prozess einer Anwendung ausgeführt wird, wenn der Dienstanbieter die Benutzeroberfläche zu unerwarteten Zeiten anzeigen muss, z. B. um das Dialogfeld **"Sprechen/Hängen"** anzuzeigen, das vom Universal Modem Driver (UNIMODEM) angezeigt wird, wenn ein Datenmodem verwendet wird, um einen interaktiven Sprachanruf über [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) (normalerweise nicht als Funktion zur Benutzeroberflächengenerierung angesehen) zu wählen.

Der Proxyanforderungshandler ist eine vollständige Telefonieanwendung, die normalerweise auf einem Telefonieserver ausgeführt wird (auf demselben Server, auf dem der Telefoniedienstanbieter für die zugeordneten Leitungsgeräte ausgeführt wird). Diese Architektur wird anstelle der WOSA-Dienstanbieterarchitektur verwendet, wenn ein bestimmter Dienst besser in einer Anwendung als in einem Treiber auf dem Server implementiert wird. Beispielsweise werden die ACD-Agent-Verwaltungsfunktionen nicht in einem Dienstanbieter, sondern in einem Proxyanforderungshandler implementiert.

Der UNIMODEM-Treiberdienstanbieter für die Modemsteuerung ist unter Windows Server 2003-Betriebssystemen, Windows XP, Windows 2000 und Windows NT verfügbar. Windows Die Telefonie umfasst auch einen generischen TSPI-Mapper (Telefoniedienstanbieterschnittstelle) im Kernelmodus, KMDDSP, mit dem Dienstanbieter als Kernelmodusgerätetreiber implementiert werden können.

 

 
