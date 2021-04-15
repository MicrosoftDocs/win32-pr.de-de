---
title: T (Taskplaner)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517282"
---
# <a name="t-task-scheduler"></a>T (Taskplaner)

a B C D [E](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**Task Objekte**
</dt> <dd>

Instanzen eines Objekts, das Methoden zum Verwalten von Aufgaben bereitstellt. Dies schließt Methoden zum Festlegen und Abrufen von Eigenschaften ein. ausführen, beenden und Löschen von Aufgaben; und das Erstellen neuer Trigger und das Abrufen von alten Triggern.

Das Task-Objekt wird durch Aufrufe von [**ischeduledworkitem::**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) up-und [**ischeduledworkitem:: gettrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger)erstellt.

</dd> <dt>

<span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**Aufgabenplaner-Objekte**
</dt> <dd>

Instanzen eines Objekts, das den Taskplaner Dienstanbieter darstellt. Dieses Objekt unterstützt zwei Schnittstellen: **IUnknown** und [**itaskscheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (zurzeit sind Tasks die einzigen Typen von Arbeits Elementen, die vom Taskplaner-Dienst unterstützt werden).

Aufgabenplaner-Objekte werden durch Aufrufe von **cokreatanstance** erstellt.

</dd> <dt>

<span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**Aufgaben auslösende Objekte**
</dt> <dd>

Instanzen eines Objekts stellt Methoden zum Festlegen und Abrufen von Task Triggern bereit. Dieses Objekt unterstützt zwei Schnittstellen: **IUnknown** und [**itaskauslöst**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).

Taskauslöserobjekte werden durch Aufrufe von [**ischeduledworkitem::**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) up-und [**ischeduledworkitem:: gettrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger)erstellt.

Siehe auch: *Trigger*.

</dd> <dt>

<span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**erfüllen**
</dt> <dd>

Ein beliebiges Element, das vom Taskplaner ausgeführt werden kann. Diese Elemente können Folgendes enthalten (wie von dem Betriebssystem unterstützt, auf dem der Task ausgeführt wird): Win32-® Anwendungen, Win16-Anwendungen, OS/2-Anwendungen, MS-DOS® Anwendungen, Batch Dateien ( \* bat), Befehls Dateien ( \* . cmd) oder ein beliebiger ordnungsgemäß registrierter Dateityp.

</dd> <dt>

<span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Ordner "Tasks"**
</dt> <dd>

Der Ordner, in dem alle Aufgaben Dateien aufgelistet werden (zurzeit sind Aufgaben die einzigen verfügbaren Arbeitselemente). Diese Dateien enthalten die Informationen über den Task. Der Name dieser Dateien gibt den Namen der Aufgabe wieder.

Sie können den Speicherort des Ordners "Tasks" aus der Registrierung abrufen, indem Sie die Daten für den folgenden Wert abrufen:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**auslöst**
</dt> <dd>

Eine Reihe von Kriterien, die die Ausführung einer Aufgabe bewirken, wenn diese erfüllt ist. Taskplaner stellt zeitbasierte und ereignisbasierte Trigger bereit, die Task Startzeiten, Wiederholungs Kriterien und andere Parameter angeben können.

</dd> <dt>

<span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**Auslöse Zeichen folgen**
</dt> <dd>

Eine Zeichenfolge, die den-Auslösers beschreibt. Diese Zeichenfolge wird vom Taskplaner-Dienst erstellt und in der Taskplaner-Benutzeroberfläche in einem Format angezeigt, das "täglich um 14 Uhr, beginnend 5/11/97" angezeigt wird.

</dd> <dt>

<span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**auslöserstrukturen**
</dt> <dd>

Die [**\_ taskauslöserstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) , die verwendet wird, wenn die Kriterien festgelegt oder abgerufen werden, durch die der- Die Kriterien umfassen, wann der Trigger ausgelöst wird, und den Typ des Auslösers.

</dd> </dl>

 

 




