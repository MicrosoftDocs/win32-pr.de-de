---
description: Die-Klausel wird zum Filtern der Ereignisse verwendet, die während des in der within-Klausel angegebenen Gruppierungs Intervalls empfangen werden.
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: Hat-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f93fbe082fb2f655dfad59d7642e1d0ff9a33e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362952"
---
# <a name="having-clause"></a>Hat-Klausel

Die-Klausel wird zum Filtern der Ereignisse verwendet, die während des in der [within-Klausel](within-clause.md)angegebenen Gruppierungs Intervalls empfangen werden. Beispielsweise könnte eine SELECT-Anweisung erstellt werden, sodass nichts zurückgegeben wird, es sei denn, es gibt mindestens 5 Ereignisse innerhalb des letzten 30 Sekunden Intervalls.

Die within-Klausel folgt sofort in der [SELECT-Anweisung](select-statement-for-event-queries.md) nach der [Group](group-clause.md) -Klausel. Die WITH-Klausel wird auf die Eigenschaft " **numofevents** " der [**\_ \_ aggregateevent**](--aggregateevent.md) -System Klasse angewendet, von der die von der Group-Klausel erstellte Gruppe ein Member ist. Die-Klausel kann alle standardmäßigen relationalen Operatoren verwenden.

Die Syntax lautet wie folgt:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

Der *EventClass* -Wert ist die Ereignisklasse, deren Member das Ereignis ist, und *value* ist der Wert für die Eigenschaft, für die eine Benachrichtigung erforderlich ist. Das Intervall ist eine Ganzzahl ohne Vorzeichen, die das Gruppierungs Intervall (in Sekunden) nach dem Empfang des ersten Ereignisses darstellt. Die Eigenschaften Liste ist eine durch Trennzeichen getrennte Liste von mindestens einer Eigenschaft, die in der Ereignisklasse enthalten ist. Der Operator ist ein beliebiger relationaler Operator. Der Konstante Wert ist eine beliebige Ganzzahl 32 ohne Vorzeichen ohne Vorzeichen, die die Anzahl der zum Filtern verwendeten Ereignisse angibt.

Wenn Sie die-Klausel verwenden, sind die WHERE-Klausel und die by-Klausel optional.

Die folgende Ereignis Abfrage fordert an, dass Benachrichtigungen der **EmailEvent** -Klasse nach dem ersten Ereignis, das von WMI empfangen wird, in ein Ereignis 300 Sekunden gruppiert werden. Außerdem sollte die Abfrage die [**\_ \_ aggregateevent**](--aggregateevent.md) -Instanz nur übermittelt werden, wenn WMI mehr als fünf e-Mail-Ereignisse in dieser 300 Sekunden empfängt.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



Im folgenden Beispiel werden alle empfangenen Ereignisse in 600 Sekunden (d. h. 10 Minuten) von der **TargetInstance** gruppiert. **SourceName** -Eigenschaft. In diesem Beispiel werden Aggregat Ereignisse nur dann übermittelt, wenn die Anzahl der von derselben Quelle empfangenen [**Win32- \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) -Ereignisse 25 überschreitet. Beachten Sie, dass der ISA-Operator bewirkt, dass die **TargetInstance** -Eigenschaft der [**\_ \_ instancecreationevent**](--instancecreationevent.md) -System Klasse eine Instanz der Win32-Klasse **\_ ntlogevent** darstellt.


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
