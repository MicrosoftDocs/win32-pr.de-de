---
title: I (Taskplaner)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8492f707a171c6811b4702d2a07de47d29482a8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517258"
---
# <a name="i-task-scheduler"></a>I (Taskplaner)

a B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**Leerlauf Bedingungen**
</dt> <dd>

Ein Zeitraum, in dem keine Benutzereingabe auf dem Computer vorhanden ist. Leerlauf Bedingungen werden der geplanten Startzeit für den Task zugeordnet.

Diese Bedingungen werden durch Aufrufen von [**ischeduledworkitem:: setFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags)festgelegt.

</dd> <dt>

<span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**Leerlauf Trigger**
</dt> <dd>

Ein ereignisbasierter-Triggertyp, der ausgelöst wird, wenn sich der Computer für einen bestimmten Zeitraum im Leerlauf befindet.

Leerlauf Trigger werden erstellt, indem der \_ tasktriggertypmember \_ der [**Task \_ triggerstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) auf Task \_ Ereignis \_ Trigger \_ im \_ Leerlauf festgelegt wird.

</dd> <dt>

<span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**Wartezeit im Leerlauf**
</dt> <dd>

Das Zeitintervall (in Minuten), das von einem Leerlauf-oder Leerlaufzustand verwendet wird. Im Leerlauf befindliche Trigger sind ereignisbasierte Trigger, die keiner geplanten Zeit zugeordnet sind. Leerlauf Bedingungen werden der geplanten Startzeit für den Task zugeordnet.

Die Leerlaufzeit wird durch einen Aufruf von [**ischeduledworkitem:: setidlewait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait)festgelegt.

</dd> </dl>

 

 




