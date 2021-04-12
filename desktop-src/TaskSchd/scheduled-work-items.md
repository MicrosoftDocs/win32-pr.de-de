---
title: Geplante Arbeitselemente
description: In der Taskplaner werden zwei Begriffe verwendet, um zu beschreiben, wie Arbeitsaufgaben und Aufgaben geplant werden können.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- Arbeitselemente Taskplaner
- Arbeitsaufgaben Taskplaner im Vergleich zu Aufgaben
- Aufgaben Taskplaner
- Aufgaben Taskplaner im Vergleich zu Arbeits Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586747e4049529dcfe747959aae994360a7b1485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309704"
---
# <a name="scheduled-work-items"></a>Geplante Arbeitselemente

Der Taskplaner verwendet zwei Begriffe, um zu beschreiben, was er planen kann: Arbeitsaufgaben und Aufgaben. In diesen beiden Begriffen ist das [*Arbeits Element*](w.md) ein allgemeinerer Begriff, der jeden Typ von Element beschreibt, der geplant werden kann. Bei einem *Arbeits Element* kann es sich um ein beliebiges Element handeln, das der Taskplaner-Dienst zu einem bestimmten Zeitpunkt ausführt, der durch die Elemente des-Elements angegeben wird.

Im Gegensatz dazu ist eine [*Aufgabe*](t.md) ein bestimmter Typ von Arbeits Element. Derzeit ist die einzige Art von geplanter Arbeitsaufgabe, die unterstützt wird, eine Aufgabe.

Die [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle enthält Methoden, die von allen Typen geplanter Arbeitselemente unterstützt werden. Kontoinformationen, Laufzeiten und Anwendungs definierte Kommentare sind z. b. Eigenschaften, die für alle Typen von Arbeits Elementen gelten können. Diese Eigenschaften können über die **ischeduledworkitem** -Schnittstelle festgelegt und abgerufen werden.

Die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle enthält Methoden, die nur von Tasks unterstützt werden.

Die Methoden der [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle werden zurzeit von der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle geerbt und in der Zukunft von anderen Arbeits Element Schnittstellen geerbt.

| Beispiele für                                              | Siehe                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Erstellen einer neuen Aufgabe.                                         | [Erstellen einer Aufgabe mit NewWorkItem-Beispiel](creating-a-task-using-newworkitem-example.md) |
| Ausführen einer vorhandenen Aufgabe                                    | [Beispiel für das Starten einer Aufgabe](starting-a-task-example.md)                                     |
| Abrufen von Eigenschaften, die für alle Typen von Arbeitsaufgaben gelten. | [Abrufen von Beispielen für Arbeits Element Eigenschaften](retrieving-work-item-property-examples.md)       |
| Festlegen von Eigenschaften, die für alle Arbeits Elementtypen gelten.    | [Festlegen von Beispielen für Arbeits Element Eigenschaften](setting-work-item-property-examples.md)             |



 

 

 




