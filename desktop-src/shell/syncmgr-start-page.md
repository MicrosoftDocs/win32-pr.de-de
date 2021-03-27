---
description: Der Synchronisierungs-Manager bietet eine zentralisierte Standardtechnologie zum Synchronisieren von Dateien für die Offline Verwendung auf einem mobilen Computer oder einem Computer, der mit einem lokalen Netzwerk verbunden ist.
title: Synchronisierungs-Manager
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994783"
---
# <a name="synchronization-manager"></a>Synchronisierungs-Manager

## <a name="purpose"></a>Zweck

Der Synchronisierungs-Manager bietet eine zentralisierte Standardtechnologie zum Synchronisieren von Dateien für die Offline Verwendung auf einem mobilen Computer oder einem Computer, der mit einem lokalen Netzwerk verbunden ist. Zusammen mit den Konnektivitätsfunktionen, Benachrichtigungen (System Ereignis Benachrichtigungsdienst) und Client seitiger Zwischenspeicherung stellt der Synchronisierungs-Manager eine Infrastruktur zur Unterstützung von mobilen Computing bereit. Anstatt jede Anwendung zu implementieren, die ihre eigene Technologie zum Zwischenspeichern und Synchronisieren von Netzwerkressourcen für die lokale Verwendung implementiert, stellt das Betriebssystem ein integriertes Modell bereit, das von allen Anwendungen verwendet werden kann. Dateien werden unabhängig vom Protokoll synchronisiert. Ein e-Mail-Programm kann z. b. seine Nachrichten mithilfe von SMTP, NMTP oder POP3 übertragen, während ein Browser http verwenden kann und eine Datenbank Remote Prozedur Aufruf (RPC) verwenden kann. Entwickler können die gemeinsame Schnittstelle für den Synchronisierungs-Manager in Ihren Anwendungen verwenden, um Dateien zwischen dem lokalen Computer des Benutzers und dem Netzwerkspeicher zu synchronisieren.

## <a name="where-applicable"></a>Anwendungsbereich

Der Synchronisierungs-Manager ist für Anwendungen vorgesehen, die in erster Linie auf mobilen Computern ausgeführt werden. Anwendungen, die auf Computern ausgeführt werden, die mit den lokalen Netzwerken mit hoher Latenz verbunden sind, können auch von der Verwendung der Synchronisierungs Verwaltung

## <a name="developer-audience"></a>Entwicklergruppe

Dieses Dokument richtet sich an Softwareentwickler, die Anwendungen für das Mobile Computing und die lokalen Netzwerke mit hoher Latenzzeit entwickeln. Dieses Dokument enthält eine vollständige Referenz aller Teile des Synchronisierungs-Managers, einschließlich der Methoden und Schnittstellen für den Synchronisierungs-Manager.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Erfordert Windows Server 2003, Windows XP, Windows 2000 oder Windows Millennium Edition (Windows Me). Auch als verteilbare Komponente für Microsoft Windows NT 4,0, Windows 98 und Windows 95 verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                       | BESCHREIBUNG                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zur Synchronisierungs Verwaltung](syncmgr-about.md)<br/>                               | Der Synchronisierungs-Manager stellt eine zentralisierte Standardtechnologie zum Synchronisieren von Dateien für die Offline Verwendung auf einem lokalen Computer bereit.<br/>     |
| [Mobile Computing-Konfigurationen](syncmgr-mobile-computing-configs.md)<br/>          | Anwendungen können den Sychronization Manager verwenden, um Dateien und Ressourcen lokal zwischengespeichert und auf mobilen Computern und Desktop Computern zu synchronisieren.<br/> |
| [Anwendungs Szenarios](syncmgr-app-scenarios.md)<br/>                               | Anwendungen und Dienste, die den Synchronisierungs-Manager verwenden können.<br/>                                                                          |
| [Architektur der Synchronisierungs Verwaltung](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [Verwenden des Synchronisierungs-Managers aus einem Programm](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [Synchronisierungs-Manager](syncmgr-reference.md)<br/>                       | Die folgenden Programmier Elemente bilden die API für den Synchronisierungs-Manager.<br/>                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum System Ereignis Benachrichtigungsdienst](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
