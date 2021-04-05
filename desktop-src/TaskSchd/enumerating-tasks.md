---
title: Auflisten von Tasks
description: Taskplaner 1,0 stellt ein Enumerationsobjekt zum Auflisten der Aufgaben im Ordner "geplante Aufgaben" bereit.
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- Aufzählen von Aufgaben Taskplaner
- Aufzählen von Aufgaben Taskplaner, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037257"
---
# <a name="enumerating-tasks"></a>Auflisten von Tasks

Taskplaner 1,0 stellt ein Enumerationsobjekt zum Auflisten der Aufgaben im [*Ordner "geplante Aufgaben*](s.md)" bereit.

> [!Note]  
> Für einen Computer mit Windows Server 2003, Windows XP oder Windows 2000 zum Erstellen, überwachen oder Steuern von Aufgaben auf einem Computer mit Windows Vista müssen bestimmte Vorgänge auf dem Computer mit Windows Vista ausgeführt werden. Weitere Informationen finden Sie unter [MSBuild-Aufgaben](tasks.md).

 

## <a name="using-the-enumeration-object"></a>Verwenden des Enumerationsobjekt

Die [**ienumworkitems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) -Schnittstelle dieses Objekts bietet Methoden zum Auflisten der Aufgaben im Ordner, zum Zurücksetzen der Enumerationsfolge auf den Anfang der Liste, zum Überspringen von Aufgaben und zum Erstellen einer Kopie des aktuellen Enumerationsobjekt für die spätere Verwendung.

Weitere Informationen zum Auflisten der Aufgaben im Ordner "geplante Aufgaben" finden Sie unter [**ienumworkitems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).

Weitere Informationen zum Zurücksetzen der Enumeration auf den Anfang der Liste finden Sie unter [**ienumworkitems:: Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).

Weitere Informationen zum Überspringen von Aufgaben finden Sie unter [**ienumworkitems:: Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).

Weitere Informationen zum Erstellen einer Kopie des aktuellen Enumerationsobjekt finden Sie unter [**ienumworkitems:: Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).

Ein Beispiel für das Auflisten der Aufgaben im Ordner "geplante Aufgaben" finden Sie unter [Beispiel](enumerating-tasks-example.md)für das Auflisten von Tasks.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Aufgabeninformationen Taskplaner 1,0](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




