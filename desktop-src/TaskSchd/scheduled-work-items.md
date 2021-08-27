---
title: Geplante Arbeitselemente
description: Der Taskplaner verwendet zwei Begriffe, um zu beschreiben, was Arbeitselemente und Aufgaben geplant werden können.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- Arbeitselemente Taskplaner
- Arbeitselemente Taskplaner im Vergleich zu Aufgaben
- Aufgaben Taskplaner
- Tasks Taskplaner im Vergleich zu Arbeitselementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19455b6d1402439403629aa5f6fca81621571fc90d9e6d8b204e741c5129414
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080430"
---
# <a name="scheduled-work-items"></a>Geplante Arbeitselemente

Die Taskplaner verwendet zwei Begriffe, um zu beschreiben, was sie planen kann: Arbeitselemente und Aufgaben. Von diesen beiden [*Begriffen ist arbeitselement*](w.md) ein allgemeinerer Begriff, der jeden Elementtyp beschreibt, der geplant werden kann. Ein *Arbeitselement kann* ein beliebiges Element sein, Taskplaner dienst ausgeführt wird, das durch die Trigger des Elements angegeben wird.

Im Gegensatz dazu ist [*eine Aufgabe*](t.md) ein bestimmter Arbeitselementtyp. Derzeit wird nur ein Task vom Typ geplantes Arbeitselement unterstützt.

Die [**IScheduledWorkItem-Schnittstelle enthält**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) Methoden, die von allen Typen geplanter Arbeitselemente unterstützt werden. Beispielsweise sind Kontoinformationen, Laufzeiten und anwendungsdefinierte Kommentare Eigenschaften, die für alle Typen von Arbeitselementen gelten können. Diese Eigenschaften können über die **IScheduledWorkItem-Schnittstelle** festgelegt und abgerufen werden.

Die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) enthält Methoden, die nur von Tasks unterstützt werden.

Die Methoden der [**IScheduledWorkItem-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) werden derzeit von der [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) geerbt und in Zukunft von anderen Arbeitselementschnittstellen geerbt.

| Beispiele für                                              | Siehe                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Erstellen einer neuen Aufgabe.                                         | [Erstellen einer Aufgabe mithilfe eines NewWorkItem-Beispiels](creating-a-task-using-newworkitem-example.md) |
| Ausführen einer vorhandenen Aufgabe.                                    | [Beispiel zum Starten einer Aufgabe](starting-a-task-example.md)                                     |
| Abrufen von Eigenschaften, die für alle Typen von Arbeitselementen gelten. | [Beispiele für das Abrufen von Arbeitselement-Eigenschaften](retrieving-work-item-property-examples.md)       |
| Festlegen von Eigenschaften, die für alle Typen von Arbeitselementen gelten.    | [Beispiele für das Festlegen von Arbeitselementeigenschaft](setting-work-item-property-examples.md)             |



 

 

 




