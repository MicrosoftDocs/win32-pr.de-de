---
description: Die GROUP-Klausel bewirkt, dass WMI eine einzelne Benachrichtigung generiert, die eine Gruppe von Ereignissen repräsentiert.
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: GROUP-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4f5f796c563376853896213c5418039ac0104d04437ec7c9e0b444db6692e60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993180"
---
# <a name="group-clause"></a>GROUP-Klausel

Die GROUP-Klausel bewirkt, dass WMI eine einzelne Benachrichtigung generiert, die eine Gruppe von Ereignissen repräsentiert. Die repräsentative Benachrichtigung ist eine Instanz der [**\_ \_ AggregateEvent-Systemklasse.**](--aggregateevent.md) Die **\_ \_ AggregateEvent-Systemklasse** enthält zwei Eigenschaften: **Representative** und **NumberOfEvents**. Die **Representative-Eigenschaft** ist ein eingebettetes Objekt, das eine der -Instanzen enthält, die während des Gruppierungsintervalls empfangen wurden, das in der [WITHIN-Klausel angegeben ist.](within-clause.md) Wenn beispielsweise ein Aggregatereignis generiert wird, um über Instanzänderungsereignisse zu benachrichtigen, enthält **Representative** eine Instanz der [**\_ \_ InstanceModificationEvent-Klasse.**](--instancemodificationevent.md) Die **NumberOfEvents-Eigenschaft** enthält die Anzahl der Ereignisse, die während des Gruppierungsintervalls empfangen wurden. Das Gruppierungsintervall gibt den Zeitraum nach dem Empfang eines anfänglichen Ereignisses an, in dem WMI ähnliche Ereignisse sammeln soll.

Die GROUP-Klausel muss eine WITHIN-Klausel enthalten, um das Gruppierungsintervall anzugeben, und kann das BY- oder HAVING-Schlüsselwort oder beides enthalten. Die GROUP-Klausel wird nach der WHERE-Klausel platziert, wie im Folgenden gezeigt:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

Der *EventClass-Wert* ist die Ereignisklasse, deren Member das Ereignis ist, und *value* ist der Wert für die Eigenschaft, für die eine Benachrichtigung erforderlich ist. Das Intervall ist eine ganze Zahl ohne Vorzeichen, die das Gruppierungsintervall nach dem Empfang des ersten Ereignisses darstellt. Die ganze Zahl ohne Vorzeichen ist eine Anzahl von Sekunden. Die Eigenschaftenliste ist eine durch Trennzeichen getrennte Liste von eigenschaften, die in der Ereignisklasse enthalten sind. *-Operator* ist ein beliebiger relationaler Operator. und *integer* ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die eine Reihe von Ereignissen angibt.

Bei Verwendung der GROUP-Klausel sind die WHERE-, BY- und HAVING-Klauseln optional.

Eine grundlegende Verwendung der GROUP-Klausel kann eine Gruppierung von Ereignissen innerhalb eines Zeitintervalls anfordern, das beginnt, wenn das erste Ereignis empfangen wird. Beispielsweise werden mit der folgenden Abfrage alle E-Mail-Ereignisse, die innerhalb von 5 Minuten gesendet werden, gegruppen. Anstatt einen Benutzer jedes Mal zu pagingen, wenn eine neue E-Mail empfangen wird, kann der permanente Consumer diese Abfrage verwenden, um den Benutzer nur zu informieren, wenn innerhalb der letzten 5 Minuten neue E-Mails empfangen wurden.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



Wenn ausführlichere Informationen erforderlich sind, können Ereignisse nach mindestens einer Eigenschaft der Ereignisklasse gruppiert werden. Die folgende Abfrage fordert an, dass E-Mail-Ereignisse mit anderen Ereignissen kombiniert werden, die denselben Wert in der **Sender-Eigenschaft** haben:


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



Eine noch höhere Detailebene kann erreicht werden, indem eine WHERE-Klausel hinzugefügt wird. Die folgende Abfrage benachrichtigt z. B. einen Benutzer über neue E-Mails von einem bestimmten Absender, der innerhalb der letzten 10 Minuten eingetroffen ist, in Kombination mit anderen Ereignissen, die den gleichen Wert in der **Importance-Eigenschaft** haben:


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



