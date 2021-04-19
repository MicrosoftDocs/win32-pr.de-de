---
description: Die folgenden Überlegungen zum Tablet PC-Threading gelten speziell für den Fall, dass Component Object Model (com) und die Automatisierung verwendet werden.
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: Überlegungen zu com-und Automatisierungs Threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344648"
---
# <a name="com-and-automation-threading-considerations"></a>Überlegungen zu com-und Automatisierungs Threading

Die folgenden Überlegungen zum Tablet PC-Threading gelten speziell für den Fall, dass Component Object Model (com) und die Automatisierung verwendet werden.

-   [Threadsicherheit](#thread-safety)
-   [STA-und MTA-Anwendungen](#sta-and-mta-applications)
-   [InkCollector und InkOverlay](#inkcollector-and-inkoverlay)
-   [Ereignis senken](#event-sinks)
-   [Ausnahmen innerhalb von Ereignis Handlern](#exceptions-within-event-handlers)
-   [Zugehörige Themen](#related-topics)

## <a name="thread-safety"></a>Threadsicherheit

Mit Ausnahme der [InkPicture](inkpicture-control.md) -und [InkEdit](inkedit-control.md) -Steuerelemente sind Tablet PC-Objekte Thread sicher und als beides gekennzeichnet. Wenn Sie als beides gekennzeichnet sind, können Sie entweder in einem Single Thread-Apartment (STA) oder einem Multithread-Apartment (MTA) ausgeführt werden.

Windows Forms verwenden das STA-Modell, da Windows Forms auf nativen Win32-Fenstern basiert, die von Natur aus Apartment Thread sind.

## <a name="sta-and-mta-applications"></a>STA-und MTA-Anwendungen

Wenn Ihre Anwendung in einem MTA ausgeführt wird oder den Free Threaded Mars Haller (FTM) verwendet, müssen Sie Thread sicheren Code schreiben. auf diese Weise können Sie jedoch bestimmte Leistungsprobleme bei der Ereignis Behandlung verbessern.

## <a name="inkcollector-and-inkoverlay"></a>InkCollector und InkOverlay

Ihre Anwendung sollte nicht ihren endgültigen Verweis auf das [**InkCollector**](inkcollector-class.md) -Objekt oder das [**InkOverlay**](inkoverlay-class.md) -Objekt freigeben und somit das Objekt direkt aus dem frei Hand Thread zerstören. Stattdessen sollte die Anwendung das **InkCollector** -Objekt oder das **InkOverlay** -Objekt aus einem Anwendungs Thread freigeben.

**Vorsicht:** Eine Anwendung, die als MTA gekennzeichnet ist oder das FTM verwendet, das direkte Aufrufe aus dem frei Hand Thread in das Apartment der Anwendung zulässt, kann den endgültigen Verweis auf das [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt direkt aus dem frei Hand Thread freigeben. Dies verursacht jedoch einen nicht BEHEB baren Anwendungsfehler.

## <a name="event-sinks"></a>Ereignis senken

Wenn Ihre Anwendung nicht FTM und ein Objekt verwendet und die zugehörige Ereignis Senke in verschiedenen Apartments erstellt wird, wird das Ereignis auf dem Thread ausgeführt, der die Ereignis Senke bedient.

## <a name="exceptions-within-event-handlers"></a>Ausnahmen innerhalb von Ereignis Handlern

Aus Tablet PC-Ereignis Handlern ausgelöste Ausnahmen werden verbraucht und sind für den Rest oder Ihre Anwendung nicht sichtbar. Ebenso werden HRESULT-Werte nicht von Tablet PC-Ereignis Handlern weitergegeben. Wenn eine Anwendung, die die com-Ebene verwendet, eine Ausnahme auslöst, wird der Hintergrund Thread beendet, und die Ausnahme geht verloren. Es werden keine weiteren Ereignishandler aufgerufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[C++ Event senken-Beispiel](c---event-sinks-sample.md)
</dt> <dt>

[Allgemeine Überlegungen zum Threading](general-threading-considerations.md)
</dt> <dt>

[Überlegungen zum Threading verwalteter Bibliotheken](managed-library-threading-considerations.md)
</dt> </dl>

 

 



