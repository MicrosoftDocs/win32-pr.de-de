---
title: Leerlauftrigger für Taskplaner 1.0
description: Ein Leerlauftrigger ist ein ereignisbasierter Trigger, der eine bestimmte Anzahl von Malen ausgelöst wird, nachdem der Computer in den Leerlauf gerät. Es gibt mehrere Bedingungen, die definieren, wann sich ein Computer im Leerlauf befindet, z. B. wenn keine Tastatur- oder Mauseingabe erfolgt.
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

Ein Leerlauftrigger ist ein ereignisbasierter Trigger, der eine bestimmte Anzahl von Malen ausgelöst wird, nachdem der Computer in den Leerlauf gerät. Es gibt mehrere Bedingungen, die definieren, wann sich ein Computer im Leerlauf befindet, z. B. wenn keine Tastatur- oder Mauseingabe erfolgt.

Leerlauftrigger werden erstellt, indem \_ TASK EVENT TRIGGER ON IDLE im TASK TRIGGER \_ \_ \_ [**\_ \_ TYPE-Member**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) der [**TASK \_ TRIGGER-Struktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) angegeben wird. Der Leerlauftrigger wird ausgelöst, wenn sich das System für den Zeitraum im Leerlauf befindet, der durch die Leerlaufwartezeit des Arbeitselements angegeben wird.

> [!Note]  
> Wenn TASK \_ EVENT TRIGGER ON IDLE angegeben \_ \_ \_ wird, werden die Member **wStartHour,** **wStartMinute** und **Type** der [**TASK \_ TRIGGER-Struktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) ignoriert.

 

Sie können die Leerlaufwartezeit eines Arbeitselements festlegen, indem Sie die [**IScheduledWorkItem::SetIdleWait-Methode**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) aufrufen. Diese Methode legt die Zeitspanne (in Minuten) fest, die das System im Leerlauf bleiben muss, bevor der Trigger ausgelöst und das Arbeitselement ausgeführt wird.

Um die Leerlaufzeit einer Aufgabe abzurufen, rufen Sie die [**IScheduledWorkItem::GetIdleWait-Methode**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgabentrigger](task-triggers.md)
</dt> </dl>

 

 




