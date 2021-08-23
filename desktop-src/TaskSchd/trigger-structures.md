---
title: Triggerstrukturen für Taskplaner 1.0
description: Taskplaner 1.0 verwendet mehrere Strukturen, um die Kriterien eines Triggers zu definieren.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a70688597f7684a6b6a0bedba90cb23d34135cd732aaed37cd74970867b3b02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002058"
---
# <a name="trigger-structures-for-task-scheduler-10"></a>Triggerstrukturen für Taskplaner 1.0

Taskplaner 1.0 verwendet mehrere Strukturen, um die Kriterien eines Triggers zu definieren.

> [!Note]  
> Weitere Informationen zu Taskplaner 2.0-Triggern finden Sie unter [Triggerschnittstellen.](trigger-interfaces.md)

 

## <a name="task-scheduler-10-structures"></a>Taskplaner 1.0-Strukturen

Die folgende Abbildung zeigt die [**TASK \_ TRIGGER-Struktur.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) Sie verfügt über drei erforderliche Member **(wBeginYear,** **wBeginMonth** und **wBeginDay),** die beim Erstellen eines neuen Triggers festgelegt werden müssen. (Um zur Referenzseite für diese Struktur zu wechseln, klicken Sie auf den Strukturnamen in der Abbildung.)

![Tasktriggerstruktur](images/tsktri1.png)

Beachten Sie, dass der **TriggerType-Member** die [**TASK TRIGGER \_ \_ TYPE-Enumeration**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) und der **Type-Member** eine **TASK TRIGGER \_ \_ UNION-Struktur** verwendet. Die **TASK \_ TRIGGER \_ TYPE-Enumeration** wird verwendet, um den Typ des Triggers anzugeben (ereignis- und zeitbasierte Triggertypen). Die [**TRIGGER \_ TYPE \_ UNION-Struktur**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) wird verwendet, um die Strukturen [**DAILY,**](/windows/desktop/api/Mstask/ns-mstask-daily) [**WEEKLY**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (Tag des Monats) und [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (Wochentag) zu kombinieren, die verwendet werden, um anzugeben, wann ein zeitbasierter Trigger ausgelöst wird.

Wenn **TriggerType** einen einmaligen oder ereignisbasierten Trigger angibt, wird der **Type-Member** ignoriert. Die [**TRIGGER \_ TYPE \_ UNION-Struktur**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) wird nur verwendet, wenn das **TriggerType-Element** einen täglichen, wöchentlichen, monats- oder monatlichen zeitbasierten Trigger angibt.

Darüber hinaus gibt die Einstellung des **Type-Members** an, welcher Member der [**TRIGGER TYPE \_ \_ UNION-Struktur**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) verwendet wird. Die folgende Abbildung zeigt die Beziehung zwischen den Werten der [**TASK \_ TRIGGER \_ TYPE-Enumeration**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) und den Membern der **TRIGGER TYPE \_ \_ STRUCTURE-Struktur.** (Um zu den Referenzseiten für diese Strukturen zu wechseln, klicken Sie auf den Strukturnamen in der Abbildung.)

![Beziehung zwischen Aufgabentriggertyp-Enumerationswerten und Membern der Triggertypstrukturstruktur](images/tsktri3.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgabentrigger](task-triggers.md)
</dt> <dt>

[Triggertypen](trigger-types.md)
</dt> <dt>

[Triggerschnittstellen](trigger-interfaces.md)
</dt> </dl>

 

 




