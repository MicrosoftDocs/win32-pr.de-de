---
description: Die Group-Klausel bewirkt, dass WMI eine einzelne Benachrichtigung generiert, um eine Gruppe von Ereignissen darzustellen.
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: Group-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 032a8e86c84c0b317b3739c0e203a249b432b0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359538"
---
# <a name="group-clause"></a>Group-Klausel

Die Group-Klausel bewirkt, dass WMI eine einzelne Benachrichtigung generiert, um eine Gruppe von Ereignissen darzustellen. Die repräsentative Benachrichtigung ist eine Instanz der System Klasse [**\_ \_ aggregateevent**](--aggregateevent.md) . Die **\_ \_ aggregateevent** -System Klasse enthält zwei Eigenschaften: " **repräsentativ** " und " **numofevents**". Die **repräsentative** Eigenschaft ist ein eingebettetes Objekt, das eine der-Instanzen enthält, die während des in der [within-Klausel](within-clause.md)angegebenen Gruppierungs Intervalls empfangen werden. Wenn z. b. ein Aggregat Ereignis generiert wird, um über instanzänderungsereignisse zu benachrichtigen, enthält der **repräsentative** eine Instanz der [**\_ \_ instancemodificationevent**](--instancemodificationevent.md) -Klasse. Die Eigenschaft " **numofevents** " enthält die Anzahl der Ereignisse, die während des Gruppierungs Intervalls empfangen wurden. Das Gruppierungs Intervall gibt den Zeitraum an, nach dem ein erstes Ereignis empfangen wird, in dem WMI ähnliche Ereignisse erfassen sollte.

Die Group-Klausel muss eine within-Klausel enthalten, um das Gruppierungs Intervall anzugeben, und kann das-oder das-Schlüsselwort oder beides enthalten. Die Group-Klausel wird nach der WHERE-Klausel eingefügt, wie im folgenden dargestellt:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

Der *EventClass* -Wert ist die Ereignisklasse, deren Member das Ereignis ist, und *value* ist der Wert für die Eigenschaft, für die eine Benachrichtigung erforderlich ist. Das Intervall ist eine Ganzzahl ohne Vorzeichen, die das Gruppierungs Intervall nach dem Empfang des ersten Ereignisses darstellt. Die ganze Zahl ohne Vorzeichen ist eine Anzahl von Sekunden. Die Eigenschaften Liste ist eine durch Trennzeichen getrennte Liste von mindestens einer Eigenschaft, die in der Ereignisklasse enthalten ist. der *Operator* ist ein beliebiger relationaler Operator. und *Integer* ist eine Ganzzahl ohne Vorzeichen, die eine ganze Zahl 32 ohne Vorzeichen angibt und eine Anzahl von Ereignissen angibt.

Wenn die Group-Klausel verwendet wird, sind die WHERE-, by-und have-Klauseln optional.

Eine grundlegende Verwendung der Group-Klausel kann eine Gruppierung von Ereignissen innerhalb eines Zeitintervalls anfordern, das beginnt, wenn das erste Ereignis empfangen wird. Beispielsweise werden in der folgenden Abfrage alle e-Mail-Ereignisse, die innerhalb von fünf Minuten gesendet werden, gruppiert. Anstatt einen Benutzer jedes Mal, wenn eine neue e-Mail empfangen wird, zu Paging, kann der permanente Consumer diese Abfrage verwenden, um den Benutzer nur dann zu benachrichtigen, wenn innerhalb der letzten 5 Minuten eine neue e-Mail eingegangen ist.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



Wenn ausführlichere Informationen erforderlich sind, können Ereignisse nach einer oder mehreren Eigenschaften der Ereignisklasse gruppiert werden. Die folgende Abfrage fordert an, dass e-Mail-Ereignisse mit anderen Ereignissen kombiniert werden, die in der **Sender** -Eigenschaft denselben Wert aufweisen:


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



Eine noch umfassendere Detailebene kann durch Hinzufügen einer WHERE-Klausel erreicht werden. Die folgende Abfrage benachrichtigt z. b. einen Benutzer über neue e-Mails von einem bestimmten Absender, der innerhalb der letzten 10 Minuten eingetroffen ist, zusammen mit anderen Ereignissen, die in der **Wichtigkeits** Eigenschaft denselben Wert aufweisen:


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



