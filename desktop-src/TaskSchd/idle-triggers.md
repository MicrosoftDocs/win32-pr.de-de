---
title: Leerlauftrigger für Taskplaner 1.0
description: Ein Trigger im Leerlauf ist ein ereignisbasierter Trigger, der nach dem Leerlauf des Computers eine bestimmte Anzahl von Malen ausgelöst wird. Es gibt mehrere Bedingungen, die definieren, wann ein Computer in den Leerlauf eintritt, z. B. wenn keine Tastatur- oder Mauseingabe erfolgt.
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349b6ce078479df841773661bfe07b098f95d1124a68803b8b472b226d9b5df6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760086"
---
# <a name="idle-triggers-for-task-scheduler-10"></a>Leerlauftrigger für Taskplaner 1.0

Ein Trigger im Leerlauf ist ein ereignisbasierter Trigger, der nach dem Leerlauf des Computers eine bestimmte Anzahl von Malen ausgelöst wird. Es gibt mehrere Bedingungen, die definieren, wann ein Computer in den Leerlauf eintritt, z. B. wenn keine Tastatur- oder Mauseingabe erfolgt.

Leerlauftrigger werden erstellt, indem TASK \_ EVENT TRIGGER ON IDLE im TASK TRIGGER \_ \_ \_ [**\_ \_ TYPE-Member**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) der [**TASK \_ TRIGGER-Struktur angegeben**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) wird. Der Leerlauftrigger wird ausgelöst, wenn das System für die Zeit, die durch die Leerlaufwartezeit des Arbeitselements angegeben wird, in den Leerlauf überläuft.

> [!Note]  
> Wenn TASK EVENT TRIGGER ON IDLE angegeben wird, werden die \_ \_ Member \_ \_ **wStartHour**, **wStartMinute** und **Type** der [**TASK \_ TRIGGER-Struktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) ignoriert.

 

Sie können die Leerlaufwartezeit eines Arbeitselements festlegen, indem Sie die [**IScheduledWorkItem::SetIdleWait-Methode**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) aufrufen. Diese Methode legt die Zeit (in Minuten) fest, die das System im Leerlauf bleiben muss, bevor der Trigger ausgelöst und das Arbeitselement ausgeführt wird.

Um die Leerlaufzeit einer Aufgabe abzurufen, rufen Sie die [**IScheduledWorkItem::GetIdleWait-Methode**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgabentrigger](task-triggers.md)
</dt> </dl>

 

 




