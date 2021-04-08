---
description: Überwachen von System Ereignis Benachrichtigungen von Programmen, die auf mobilen Computern ausgeführt werden, um die Bandbreite und Latenz der Netzwerkverbindung zu ermitteln Schreiben Sie optimierte Anwendungen für Mobile Computing und LANs mit hoher Latenz.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Benachrichtigungsdienst für Systemereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960447"
---
# <a name="system-event-notification-service"></a>Benachrichtigungsdienst für Systemereignisse

## <a name="purpose"></a>Zweck

Anwendungen, die zur Verwendung durch mobile Benutzer entwickelt wurden, benötigen einen eindeutigen Satz von Konnektivitätsfunktionen und-Benachrichtigungen. In der Vergangenheit waren diese individuellen Anwendungen erforderlich, um diese Features intern zu implementieren. Der System Event Notification Service (Sens) stellt diese Funktionen jetzt im Betriebs System bereit und erstellt eine einheitliche Konnektivität und Benachrichtigungs Schnittstelle für Anwendungen. Die Verwendung von Sens-Entwicklern kann die Verbindungs Bandbreite und Latenz Informationen aus Ihrer Anwendung heraus ermitteln und den Betrieb der Anwendung basierend auf diesen Bedingungen optimieren.

## <a name="where-applicable"></a>Anwendungsbereich

Die Konnektivitätsfunktionen und Benachrichtigungen von Sens sind für Anwendungen nützlich, die für mobile Computer oder Computer geschrieben wurden, die mit lokalen Netzwerken mit hoher Latenz verbunden sind.

## <a name="developer-audience"></a>Entwicklergruppe

Dieses Dokument richtet sich an Softwareentwickler, die Anwendungen für das Mobile Computing und die lokalen Netzwerke mit hoher Latenzzeit entwickeln. Dieses Dokument enthält eine vollständige Referenz aller Teile des System Ereignis Benachrichtigungs Diensts, einschließlich des Sens-Objekts und der unterstützenden Methoden.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Erfordert Microsoft Windows XP oder höher. Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Schnittstelle oder Funktion erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der Dokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                              | BESCHREIBUNG                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Übersicht](about-system-event-notification-service.md)<br/> | Allgemeine Informationen zum System Ereignis Benachrichtigungsdienst.<br/>               |
| [Verweis](sens-reference.md)<br/>                         | Dokumentation der Methoden und Schnittstellen des System Ereignis Benachrichtigungs Diensts.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ieventabonnement**](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
