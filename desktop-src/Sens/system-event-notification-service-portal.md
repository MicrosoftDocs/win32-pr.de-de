---
description: Überwachen Sie Systemereignisbenachrichtigungen von Programmen, die auf mobilen Computern ausgeführt werden, um die Netzwerkverbindungsbandbreite und -latenz zu ermitteln. Schreiben sie optimierte Anwendungen für mobiles Computing und LANs mit hoher Latenz.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Benachrichtigungsdienst für Systemereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e76ee51ea0e7a341f0205528e9083cb1f6c0420f941025ec71c32c9154850b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003928"
---
# <a name="system-event-notification-service"></a>Benachrichtigungsdienst für Systemereignisse

## <a name="purpose"></a>Zweck

Anwendungen, die für die Verwendung durch mobile Benutzer entwickelt wurden, erfordern einen eindeutigen Satz von Konnektivitätsfunktionen und Benachrichtigungen. In der Vergangenheit waren diese einzelnen Anwendungen erforderlich, um diese Features intern zu implementieren. Der Systemereignisbenachrichtigungsdienst (System Event Notification Service, SENS) stellt diese Funktionen jetzt im Betriebssystem bereit und erstellt eine einheitliche Konnektivitäts- und Benachrichtigungsschnittstelle für Anwendungen. Mithilfe von SENS können Entwickler informationen zur Verbindungsbandbreite und -latenz innerhalb ihrer Anwendung ermitteln und den Betrieb der Anwendung basierend auf diesen Bedingungen optimieren.

## <a name="where-applicable"></a>Anwendungsbereich

Die Konnektivitätsfunktionen und Benachrichtigungen von SENS sind nützlich für Anwendungen, die für mobile Computer oder Computer geschrieben wurden, die mit lokalen Netzwerken mit hoher Latenz verbunden sind.

## <a name="developer-audience"></a>Entwicklergruppe

Dieses Dokument richtet sich an Softwareentwickler, die Anwendungen für mobiles Computing und lokale Netzwerke mit hoher Latenz entwickeln. Dieses Dokument enthält eine vollständige Referenz zu allen Teilen des Systemereignisbenachrichtigungsdiensts, einschließlich des SENS-Objekts und der unterstützenden Methoden.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Erfordert Microsoft Windows XP oder höher. Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Schnittstelle oder Funktion erforderlich sind, finden Sie im Abschnitt Anforderungen der Dokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                              | Beschreibung                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Übersicht](about-system-event-notification-service.md)<br/> | Allgemeine Informationen zum Systemereignisbenachrichtigungsdienst.<br/>               |
| [Referenz](sens-reference.md)<br/>                         | Dokumentation der Methoden und Schnittstellen des Systemereignisbenachrichtigungsdiensts.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IEventSubscription**](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
