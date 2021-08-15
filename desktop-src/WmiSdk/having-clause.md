---
description: Die HAVING-Klausel wird verwendet, um die Ereignisse zu filtern, die während des in der WITHIN-Klausel angegebenen Gruppierungsintervalls empfangen werden.
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: HAVING-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2662ea337c5664130eb9973c049431daedefe3c947c45eb397a950522fea6bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993160"
---
# <a name="having-clause"></a>HAVING-Klausel

Die HAVING-Klausel wird verwendet, um die Ereignisse zu filtern, die während des gruppierungsintervalls empfangen werden, das in der [WITHIN-Klausel angegeben ist.](within-clause.md) Beispielsweise könnte eine SELECT-Anweisung so erstellt werden, dass sie nichts zurückgibt, es sei denn, innerhalb der letzten 30 Sekunden wurden INTERVALL mindestens 5 Ereignisse durchgeführt.

Die WITHIN-Klausel folgt unmittelbar in der [SELECT-Anweisung nach](select-statement-for-event-queries.md) der [GROUP-Klausel.](group-clause.md) Die HAVING-Klausel arbeitet mit der **NumberOfEvents-Eigenschaft** der [**\_ \_ AggregateEvent-Systemklasse,**](--aggregateevent.md) deren Mitglied die von der GROUP-Klausel erstellte Gruppe ist. Die HAVING-Klausel kann alle relationalen Standardoperatoren verwenden.

Die Syntax ist wie folgt:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

Der *EventClass-Wert* ist die Ereignisklasse, deren Member das Ereignis ist, und *value* ist der Wert für die Eigenschaft, für die eine Benachrichtigung erforderlich ist. Das Intervall ist eine ganze Zahl ohne Vorzeichen, die das Gruppierungsintervall (in Sekunden) nach dem Empfang des ersten Ereignisses darstellt. Die Eigenschaftenliste ist eine durch Trennzeichen getrennte Liste von eigenschaften, die in der Ereignisklasse enthalten sind. Der -Operator ist ein beliebiger relationaler Operator. Der konstante Wert ist eine beliebige 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der zum Filtern verwendeten Ereignisse angibt.

Bei Verwendung der HAVING-Klausel sind die WHERE- und BY-Klauseln optional.

Die folgende Ereignisabfrage fordert an, dass Benachrichtigungen der **EmailEvent-Klasse** 300 Sekunden nach dem ersten Ereignis, das WMI empfängt, in ein Ereignis eingekreist werden. Außerdem fordert die Abfrage an, dass die [**\_ \_ AggregateEvent-Instanz**](--aggregateevent.md) nur übermittelt werden soll, wenn WMI in diesen 300 Sekunden mehr als fünf E-Mail-Ereignisse empfängt.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



Im folgenden Beispiel werden alle Von **TargetInstance** empfangenen Ereignisse in 600 Sekunden (d. h. 10 Minuten) unterteilt. **SourceName-Eigenschaft.** In diesem Beispiel werden Aggregatereignisse nur übermittelt, wenn die Anzahl der [**Win32 \_ NTLogEvent-Ereignisse,**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) die von derselben Quelle empfangen werden, 25 überschreitet. Beachten Sie, dass der ISA-Operator bewirkt, dass die **TargetInstance-Eigenschaft** der [**\_ \_ InstanceCreationEvent-Systemklasse**](--instancecreationevent.md) eine Instanz der **Win32 \_ NTLogEvent-Klasse** repräsentiert.


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
