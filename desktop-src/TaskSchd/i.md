---
title: I (Taskplaner)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14bec8dd745aee798ebb6aa9cb296d7a0990b85b44562fb94ea844d2d5d3397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072640"
---
# <a name="i-task-scheduler"></a>I (Taskplaner)

A B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**Leerlaufbedingungen**
</dt> <dd>

Ein Zeitraum, in dem keine Benutzereingaben auf dem Computer vorhanden sind. Leerlaufbedingungen sind der geplanten Startzeit für den Task zugeordnet.

Diese Bedingungen werden durch Aufrufen von [**IScheduledWorkItem::SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags)festgelegt.

</dd> <dt>

<span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**Trigger im Leerlauf**
</dt> <dd>

Ein ereignisbasierter Trigger, der ausgelöst wird, wenn sich der Computer für einen bestimmten Zeitraum im Leerlauf befindet.

Leerlauftrigger werden erstellt, indem der \_ TASK TRIGGER \_ TYPE-Member der [**\_ TASKTRIGGER-Struktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) auf TASK EVENT TRIGGER ON IDLE festgelegt \_ \_ \_ \_ wird.

</dd> <dt>

<span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**Leerlaufwartezeit**
</dt> <dd>

Das Zeitintervall (in Minuten), das von einem Leerlauftrigger oder einer Leerlaufbedingung verwendet wird. Leerlauftrigger sind ereignisbasierte Trigger, die keiner geplanten Zeit zugeordnet sind. Leerlaufbedingungen sind der geplanten Startzeit für den Task zugeordnet.

Die Leerlaufzeit wird durch einen Aufruf von [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait)festgelegt.

</dd> </dl>

 

 




