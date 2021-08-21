---
description: Zeitachsenobjekte
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Zeitachsenobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbcf3496770dee7664e08ffabe6537356c7b37ad13abee1dce149698748745e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072304"
---
# <a name="timeline-objects"></a>Zeitachsenobjekte

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Jeder Objekttyp in der Zeitachse ( Quelle, Nachverfolgung, Effekt usw.) ist ein eindeutiges COM-Objekt. Eine Anwendung erstellt sie jedoch nicht mithilfe der **CoCreateInstance-Funktion.** Stattdessen wird die [**IAMTimeline::CreateEmptyNode-Methode**](iamtimeline-createemptynode.md) aufruft. Diese Methode erstellt ein Objekt des angeforderten Typs, initialisiert es und gibt einen Zeiger auf das -Objekt zurück. Weitere Informationen finden Sie unter [Erstellen einer Zeitachse.](constructing-a-timeline.md)

Jedes Zeitachsenobjekt macht die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) verfügbar. Darüber hinaus unterstützen die verschiedenen Objekttypen ihre eigenen spezialisierten Schnittstellen:

-   Quelle: [ **IAMTimelineSrc**](iamtimelinesrc.md)
-   Track: [ **IAMTimelineTrack**](iamtimelinetrack.md)
-   Komposition: [ **IAMTimelineComp**](iamtimelinecomp.md)
-   Gruppe: [**IAMTimelineComp,**](iamtimelinecomp.md) [**IAMTimelineGroup**](iamtimelinegroup.md)
-   Auswirkung: [ **IAMTimelineEffect**](iamtimelineeffect.md)
-   Übergang: [ **IAMTimelineTrans**](iamtimelinetrans.md)

Beachten Sie, dass Gruppen eine Art von Komposition sind, sodass sie [**IAMTimelineComp**](iamtimelinecomp.md)sowie ihre eigene [**IAMTimelineGroup-Schnittstelle**](iamtimelinegroup.md) unterstützen.

Zusätzlich zu den zuvor aufgeführten Schnittstellen machen Zeitachsenobjekte andere sekundäre Schnittstellen verfügbar. Diese Schnittstellen bestimmen die Beziehungen zwischen den Objekttypen.



| Schnittstelle                                                  | Bedeutung                                                                                                       | Verfügbar gemacht von                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Das -Objekt ist eine virtuelle Spur. Virtuelle Spuren können sich in Kompositionen befinden und andere Zeitachsenobjekte enthalten. | Komposition, Nachverfolgung                |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | Das -Objekt kann Auswirkungen haben.                                                                                  | Composition, Track, Source        |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | Das -Objekt kann Übergänge haben.                                                                              | Komposition, Nachverfolgung                |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | Das -Objekt kann in zwei -Objekte aufgeteilt werden.                                                                     | Track, Source, Effect, Transition |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Zeitachsenkomponenten](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



