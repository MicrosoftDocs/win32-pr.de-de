---
description: Dienstanbieter implementieren ausführliche telefoniesteuerungssteuerelemente. Ein Telefoniedienstanbieter (TSP) stellt Callcenter-Steuerelemente und einen Medien Dienstanbieter bereit, sofern vorhanden, die Kontrolle über den Mediendaten Strom.
ms.assetid: eb63d55e-4a2b-4bc0-8001-99772f418d72
title: Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424c11d5b99af7440835e8822a5631e1b36f48cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960993"
---
# <a name="service-providers"></a>Dienstanbieter

Dienstanbieter implementieren ausführliche telefoniesteuerungssteuerelemente. Ein Telefoniedienstanbieter (TSP) stellt Callcenter-Steuerelemente und einen Medien Dienstanbieter bereit, sofern vorhanden, die Kontrolle über den Mediendaten Strom.

Alle Telefoniedienstanbieter werden im tapisrv-Prozess ausgeführt. Dienstanbieter können Threads im tapisrv-Kontext erstellen, wenn Sie für Ihre Arbeit benötigt werden, und sicher sein, dass keine der von Ihnen erstellten Ressourcen durch das Beenden einer einzelnen Anwendung zerstört werden. Der TAPI-Server übersetzt Anwendungs Befehle nach Bedarf in einen konsistenten Satz von Befehlen, die als TSPI (Telefonie Service Provider Interface) bezeichnet werden.

Media Service-Anbieter werden im Prozessbereich der Anwendung ausgeführt und ermöglichen so eine schnelle Antwort, die manchmal in mediensteuer Elementen erforderlich ist. Die TAPI-dll ermöglicht eine konsistente Einhaltung der MSPi (Media Service Provider Interface).

Ausführlichere Informationen zu den Dienstanbietern finden Sie unter [Übersicht über den TAPI-Dienstanbieter](./tapi-service-provider-overview.md).

Unterhalb der Telefoniedienstanbieter-dll kann der Dienstanbieter beliebige Systemfunktionen oder andere erforderliche Komponenten verwenden. Zu diesen Funktionen gehören " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " und " [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)", die mit unabhängigen Hardwarehersteller entworfenen Kernelmoduskomponenten und-Diensten sowie Standardgeräten wie seriellen und parallelen Ports zum Steuern externer, lokal verbundener Geräte funktionieren. Sie können auch auf Netzwerkdienste (z. b. RPC, Windows Sockets und Named Pipes) für Client/Server-Telefonie zugreifen.

Die Benutzeroberflächen-DLL des Telefoniedienstanbieters wird von TAPI in den Prozess einer Anwendung geladen, die eine der Dienstanbieter Funktionen aufruft, die ein Dialogfeld anzeigen können (z. [**b. TSPI \_ lineconfigdialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)). Der Dienstanbieter kann auch bewirken, dass die zugehörige UI-DLL geladen und im Prozess der Anwendung ausgeführt wird, wenn der Dienstanbieter die Benutzeroberfläche zu unerwarteten Zeiten anzeigen muss. beispielsweise, um das vom Universal Modem Driver (Unimodem) angezeigte Dialogfeld zum durch **Suchen/** einblenden anzuzeigen, wenn ein Datenmodem verwendet wird, um einen interaktiven Sprachanruf mithilfe von [**TSPI \_ linemakecall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) festzuhalten (wird normalerweise nicht als UI-Generierungs Funktion angesehen).

Der Proxy Anforderungs Handler ist eine vollständige Telefonieanwendung, die normalerweise auf einem Telefonieserver (dem gleichen Server, auf dem der Telefoniedienstanbieter für die zugeordneten Zeilen Geräte ausgeführt wird) ausgeführt wird. Diese Architektur wird anstelle der Architektur des WOSA-Dienstanbieters verwendet, wenn ein bestimmter Dienst in einer Anwendung besser implementiert ist als bei einem Treiber auf dem Server. Beispielsweise werden die Verwaltungsfunktionen für den ACD-Agent in einen Proxy Anforderungs Handler und nicht in einen Dienstanbieter implementiert.

Der Unimodem-Treiber Dienstanbieter für die Modem Steuerung ist unter den Betriebssystemen Windows Server 2003, Windows XP, Windows 2000 und Windows NT verfügbar. Windows-Telefonieinformationen beinhalten außerdem einen generischen TSPI-Mapper (Kernel-Mode Telefonie Service Provider Interface), kmddsp, mit dem Dienstanbieter als Kernelmodustreiber implementiert werden können.

 

 
