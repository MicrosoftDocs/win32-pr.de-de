---
description: Timeline-Objekte
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Timeline-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580286b31afd77f064411dd29d60a62b80bfb51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350178"
---
# <a name="timeline-objects"></a>Timeline-Objekte

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Jeder Objekttyp in der Zeitachse – Quelle, Track, Effect usw. – ist ein eindeutiges com-Objekt. Eine Anwendung erstellt Sie jedoch nicht mithilfe der **cokreatanstance** -Funktion. Stattdessen wird die [**iamtimeline:: erkreateemptynode**](iamtimeline-createemptynode.md) -Methode aufgerufen. Diese Methode erstellt ein Objekt des angeforderten Typs, initialisiert es und gibt einen Zeiger auf das-Objekt zurück. Weitere Informationen finden Sie unter [Erstellen einer Zeitachse](constructing-a-timeline.md).

Jedes Zeitachsen Objekt macht die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle verfügbar. Außerdem unterstützen die verschiedenen Objekttypen ihre eigenen spezialisierten Schnittstellen:

-   Quelle: [ **iamtimelinesrc**](iamtimelinesrc.md)
-   Nachverfolgung: [ **iamtimelinetrack**](iamtimelinetrack.md)
-   Komposition: [ **iamtimelinecomp**](iamtimelinecomp.md)
-   Gruppe: [**iamtimelinecomp**](iamtimelinecomp.md), [**iamtimelinegroup**](iamtimelinegroup.md)
-   Auswirkung: [ **iamtimelineeffect**](iamtimelineeffect.md)
-   Übergang: [ **iamtimelinetrans**](iamtimelinetrans.md)

Beachten Sie, dass Gruppen eine Art der Komposition sind, sodass Sie [**iamtimelinecomp**](iamtimelinecomp.md)und ihre eigene [**iamtimelinegroup**](iamtimelinegroup.md) -Schnittstelle unterstützen.

Zusätzlich zu den zuvor aufgelisteten Schnittstellen stellen Zeitachsen Objekte andere sekundäre Schnittstellen zur Verfügung. Diese Schnittstellen bestimmen die Beziehungen zwischen den Objekttypen.



| Schnittstelle                                                  | Bedeutung                                                                                                       | Verfügbar von                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [**Iamtimelinevirtualtrack**](iamtimelinevirtualtrack.md) | Das-Objekt ist ein virtueller Titel. Virtuelle Spuren können sich innerhalb von Kompositionen befinden und andere Zeitachsen Objekte enthalten. | Komposition, Nachverfolgung                |
| [**Iamtimelineeffectable**](iamtimelineeffectable.md)     | Das-Objekt kann Auswirkungen haben.                                                                                  | Komposition, Nachverfolgung, Quelle        |
| [**Iamtimelinetransable**](iamtimelinetransable.md)       | Das-Objekt kann über Übergänge verfügen.                                                                              | Komposition, Nachverfolgung                |
| [**Iamtimelinesplicustom**](iamtimelinesplittable.md)     | Das-Objekt kann in zwei-Objekte aufgeteilt werden.                                                                     | Track, Source, Effect, Transition |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Zeitachsen Komponenten](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



