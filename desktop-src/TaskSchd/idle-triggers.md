---
title: Leerlauf Trigger für Taskplaner 1,0
description: Ein im Leerlauf befindlich ausgelöster Triggertyp ist ein ereignisbasierter-Triggertyp, der nach dem Ausfall des Computers nach dem Leerlauf ausgelöst wird. Es gibt mehrere Bedingungen, die definieren, wann ein Computer in den Leerlauf wechselt, z. b. wenn keine Tastatur-oder Maus Eingaben auftritt.
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a19f3f6d474a9463667316e353a4803ab8fa9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342253"
---
# <a name="idle-triggers-for-task-scheduler-10"></a>Leerlauf Trigger für Taskplaner 1,0

Ein im Leerlauf befindlich ausgelöster Triggertyp ist ein ereignisbasierter-Triggertyp, der nach dem Ausfall des Computers nach dem Leerlauf ausgelöst wird. Es gibt mehrere Bedingungen, die definieren, wann ein Computer in den Leerlauf wechselt, z. b. wenn keine Tastatur-oder Maus Eingaben auftritt.

Leerlauf Trigger werden erstellt, indem ein \_ Task \_ Ereignis \_ Trigger \_ im Leerlauf im Member des [**\_ tasktriggertyps \_**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) der [**Task \_ triggerstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) angegeben wird. Der Leerlauf-Triggervorgang wird ausgelöst, wenn das System für den Zeitraum, der durch die Leerlauf Wartezeit der Arbeitsaufgabe angegeben wird, in den Leerlauf wechselt.

> [!Note]  
> Wenn ein Task Ereignis-Auslösung \_ \_ \_ im \_ Leerlauf angegeben wird, werden die **Member wstarthour**, **wstartminute** und Type der [**Task \_ auslöserstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) ignoriert. 

 

Sie können die Leerlauf Wartezeit eines Arbeits Elements festlegen, indem Sie die [**ischeduledworkitem:: setidlewait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) -Methode aufrufen. Mit dieser Methode wird die Zeitspanne (in Minuten) festgelegt, in der sich das System im Leerlauf befinden muss, bevor der-auslösen ausgelöst und die Arbeitsaufgabe ausgeführt wird.

Um die Leerlaufzeit einer Aufgabe abzurufen, rufen Sie die [**ischeduledworkitem:: getidlewait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) -Methode auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Task Trigger](task-triggers.md)
</dt> </dl>

 

 




