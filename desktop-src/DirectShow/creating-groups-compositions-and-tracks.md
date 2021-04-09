---
description: Erstellen von Gruppenkompositionen und-Spuren
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: Erstellen von Gruppenkompositionen und-Spuren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2808c2d096b52ad73da7d518d703bc25103751d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860506"
---
# <a name="creating-groups-compositions-and-tracks"></a>Erstellen von Gruppenkompositionen und-Spuren

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Gruppen, Kompositionen und Spuren sind die zwischen Ebenen zwischen der Zeitachse und den Quell Clips. Sie unterscheiden sich durch den Objekttyp, den Sie enthalten können.

-   Spuren enthalten Quell Objekte.
-   Die Komposition enthält Spuren und andere Kompositionen, aber keine Quell Objekte.
-   Gruppen sind Kompositionen der obersten Ebene. Gruppen enthalten Kompositionen und Spuren, aber die Komposition darf keine Gruppen enthalten.
-   Ein *virtueller Titel* ist ein beliebiges Objekt, das sich in einer Komposition oder einer Gruppe befinden kann. Dies schließt Titel und Kompositionen ein.

Diese Objekte machen die folgenden Schnittstellen verfügbar:



| Schnittstelle                                                  | Verfügbar von           |
|------------------------------------------------------------|----------------------|
| [**Iamtimelinetrack**](iamtimelinetrack.md)               | Spuren               |
| [**Iamtimelinevirtualtrack**](iamtimelinevirtualtrack.md) | Spuren, Kompositionen |
| [**Iamtimelinecomp**](iamtimelinecomp.md)                 | Komposition, Gruppen |
| [**Iamtimelinegroup**](iamtimelinegroup.md)               | Gruppen               |



 

Diese Schnittstellen enthalten die Methoden zum Hinzufügen von Objekten zur Zeitachse.

-   [**Iamtimeline:: addgroup**](iamtimeline-addgroup.md): Fügt eine Gruppe in die Zeitachse ein.
-   [**Iamtimelinecomp:: vtrackinsbefore**](iamtimelinecomp-vtrackinsbefore.md): Fügt einen virtuellen Track in eine Komposition oder eine Gruppe ein.
-   [**Iamtimelinetrack:: srcadd**](iamtimelinetrack-srcadd.md): Fügt eine Quelle in eine Spur ein.

Der folgende Code fügt z. b. einen neuen Track in eine Gruppe ein. Wie in der obigen Tabelle gezeigt, wird eine Gruppe als eine Art Komposition betrachtet, und eine Spur ist eine Art virtueller Nachverfolgung. Wenn Sie also den Track in die Gruppe einfügen möchten, müssen Sie die Gruppe nach ihrer **iamtimelinecomp** -Schnittstelle Abfragen und die **iamtimelinecomp:: vtrackinsbefore** -Methode aufrufen.


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



Der zweite Parameter für **vtrackinsbefore** gibt die Priorität des virtuellen Titels an. Prioritätsstufen beginnen bei Null. Wenn Sie den Wert – 1 angeben, wird die virtuelle Spur am Ende der Prioritäts Liste eingefügt. Wenn Sie einen Wert angeben, bei dem bereits eine virtuelle Spur vorhanden ist, wird von diesem Punkt aus die Liste um eine Prioritäts Ebene nach unten verschoben. Fügen Sie eine virtuelle Spur nicht mit einer Priorität ein, die größer als die Anzahl der virtuellen Spuren ist, da dies zu undefiniertem Verhalten führt.

Um ein Objekt dauerhaft aus der Zeitachse zu löschen, nennen Sie [**iamtimelineobj:: RemoveAll**](iamtimelineobj-removeall.md) für das Objekt. Diese Methode entfernt das-Objekt und alle zugehörigen untergeordneten Elemente. Um ein Objekt zu entfernen, um es an anderer Stelle in der Zeitachse wiederherzustellen, müssen Sie stattdessen [**iamtimelineobj:: Remove**](iamtimelineobj-remove.md) aufrufen. Anders als **RemoveAll** löscht diese Methode nicht die untergeordneten Elemente des Objekts. Um alles aus der Zeitachse zu entfernen, nennen Sie [**iamtimeline:: clearallgroups**](iamtimeline-clearallgroups.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Zeitachse](constructing-a-timeline.md)
</dt> </dl>

 

 



