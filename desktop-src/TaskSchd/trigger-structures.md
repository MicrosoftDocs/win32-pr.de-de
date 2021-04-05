---
title: Auslöse Strukturen für Taskplaner 1,0
description: Taskplaner 1,0 verwendet mehrere Strukturen, um die Kriterien eines Auslösers zu definieren.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a03f28f85782d87ee3349582929babe6f907e8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037094"
---
# <a name="trigger-structures-for-task-scheduler-10"></a>Auslöse Strukturen für Taskplaner 1,0

Taskplaner 1,0 verwendet mehrere Strukturen, um die Kriterien eines Auslösers zu definieren.

> [!Note]  
> Weitere Informationen zu Taskplaner 2,0-Triggern finden Sie unter [triggerschnittstellen](trigger-interfaces.md).

 

## <a name="task-scheduler-10-structures"></a>Taskplaner 1,0-Strukturen

In der folgenden Abbildung ist die Struktur des [**Task \_ Auslösers**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) dargestellt. Er verfügt über drei erforderliche Mitglieder (**wbeginyear**, **wbeginmonth** und **wbeginday**), die beim Erstellen eines neuen-Auslösers festgelegt werden müssen. (Um zur Referenzseite für diese Struktur zu springen, klicken Sie in der Abbildung auf den Struktur Namen.)

![Task auslöserstruktur](images/tsktri1.png)

Beachten Sie, dass **der TriggerType** -Member die Enumeration des [**\_ tasktriggertyps \_**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) verwendet und der **Typmember** eine **Aufgaben \_ Trigger- \_ Union** -Struktur verwendet. Die Enumeration des **\_ taskauslösers \_** wird verwendet, um den Typ des Auslösers anzugeben (Ereignis-und zeitbasierte Auslösertypen). Die Union-Struktur des [**\_ triggertyps \_**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) wird verwendet, um die Strukturen [**täglich**](/windows/desktop/api/Mstask/ns-mstask-daily), [**wöchentlich**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**monthlydate**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (Tag of month) und [**monthlydow**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (Day of week) zu kombinieren, mit denen angegeben wird, wann ein zeitbasierter Trigger ausgelöst wird.

Wenn **TriggerType** einen einmaligen zeitbasierten Trigger oder einen ereignisbasierten Trigger angibt, wird der **Typmember** ignoriert. Die Union-Struktur des [**\_ triggertyps \_**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) wird nur verwendet, wenn der **TriggerType** -Member einen Tages-, Wochen-, Monats-oder Monats Tags-zeitbasierten Trigger angibt.

Außerdem gibt die Einstellung des **Typmembers** an, welcher Member der [**\_ auslösertyp- \_ Union**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) -Struktur verwendet wird. In der folgenden Abbildung wird die Beziehung zwischen den Werten der [**\_ \_ Aufgabentyp**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) -Enumeration des Tasks und den Membern der **Struktur der \_ auslösertyp \_ Struktur** veranschaulicht. (Um zu den Referenzseiten für diese Strukturen zu springen, klicken Sie in der Abbildung auf den Struktur Namen.)

![Beziehung zwischen den Enumerationswerten des Task Auslösers und Membern der auslösertyp-Struktur Struktur](images/tsktri3.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Task Trigger](task-triggers.md)
</dt> <dt>

[Auslösertypen](trigger-types.md)
</dt> <dt>

[Auslöse Schnittstellen](trigger-interfaces.md)
</dt> </dl>

 

 




