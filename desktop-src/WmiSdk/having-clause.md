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
# <a name="having-clause"></a><span data-ttu-id="4486d-103">Hat-Klausel</span><span class="sxs-lookup"><span data-stu-id="4486d-103">HAVING Clause</span></span>

<span data-ttu-id="4486d-104">Die-Klausel wird zum Filtern der Ereignisse verwendet, die während des in der [within-Klausel](within-clause.md)angegebenen Gruppierungs Intervalls empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="4486d-104">The HAVING clause is used to filter the events that are received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="4486d-105">Beispielsweise könnte eine SELECT-Anweisung erstellt werden, sodass nichts zurückgegeben wird, es sei denn, es gibt mindestens 5 Ereignisse innerhalb des letzten 30 Sekunden Intervalls.</span><span class="sxs-lookup"><span data-stu-id="4486d-105">For example, a SELECT statement could be constructed so that it returns nothing unless there HAVE been at least 5 events within the past 30 second INTERVAL.</span></span>

<span data-ttu-id="4486d-106">Die within-Klausel folgt sofort in der [SELECT-Anweisung](select-statement-for-event-queries.md) nach der [Group](group-clause.md) -Klausel.</span><span class="sxs-lookup"><span data-stu-id="4486d-106">The WITHIN clause follows immediately in the [SELECT statement](select-statement-for-event-queries.md) after the [GROUP](group-clause.md) clause.</span></span> <span data-ttu-id="4486d-107">Die WITH-Klausel wird auf die Eigenschaft " **numofevents** " der [**\_ \_ aggregateevent**](--aggregateevent.md) -System Klasse angewendet, von der die von der Group-Klausel erstellte Gruppe ein Member ist.</span><span class="sxs-lookup"><span data-stu-id="4486d-107">The HAVING clause operates on the **NumberOfEvents** property of the [**\_\_AggregateEvent**](--aggregateevent.md) system class, of which the group created by the GROUP clause is a member.</span></span> <span data-ttu-id="4486d-108">Die-Klausel kann alle standardmäßigen relationalen Operatoren verwenden.</span><span class="sxs-lookup"><span data-stu-id="4486d-108">The HAVING clause can use all of the standard relational operators.</span></span>

<span data-ttu-id="4486d-109">Die Syntax lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4486d-109">The syntax is as follows:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

<span data-ttu-id="4486d-110">Der *EventClass* -Wert ist die Ereignisklasse, deren Member das Ereignis ist, und *value* ist der Wert für die Eigenschaft, für die eine Benachrichtigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4486d-110">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="4486d-111">Das Intervall ist eine Ganzzahl ohne Vorzeichen, die das Gruppierungs Intervall (in Sekunden) nach dem Empfang des ersten Ereignisses darstellt.</span><span class="sxs-lookup"><span data-stu-id="4486d-111">The interval is an unsigned integer that represents the grouping interval (in seconds) after receiving the first event.</span></span> <span data-ttu-id="4486d-112">Die Eigenschaften Liste ist eine durch Trennzeichen getrennte Liste von mindestens einer Eigenschaft, die in der Ereignisklasse enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4486d-112">The property list is a comma-delimited list of one or more properties that are included in the event class.</span></span> <span data-ttu-id="4486d-113">Der Operator ist ein beliebiger relationaler Operator.</span><span class="sxs-lookup"><span data-stu-id="4486d-113">The operator is any relational operator.</span></span> <span data-ttu-id="4486d-114">Der Konstante Wert ist eine beliebige Ganzzahl 32 ohne Vorzeichen ohne Vorzeichen, die die Anzahl der zum Filtern verwendeten Ereignisse angibt.</span><span class="sxs-lookup"><span data-stu-id="4486d-114">The constant value is any unsigned 32-bit integer indicating the number of events used for filtering.</span></span>

<span data-ttu-id="4486d-115">Wenn Sie die-Klausel verwenden, sind die WHERE-Klausel und die by-Klausel optional.</span><span class="sxs-lookup"><span data-stu-id="4486d-115">When using the HAVING clause, the WHERE and BY clauses are optional.</span></span>

<span data-ttu-id="4486d-116">Die folgende Ereignis Abfrage fordert an, dass Benachrichtigungen der **EmailEvent** -Klasse nach dem ersten Ereignis, das von WMI empfangen wird, in ein Ereignis 300 Sekunden gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="4486d-116">The following event query requests that notifications of the **EmailEvent** class be grouped into one event 300 seconds after the first event that WMI receives.</span></span> <span data-ttu-id="4486d-117">Außerdem sollte die Abfrage die [**\_ \_ aggregateevent**](--aggregateevent.md) -Instanz nur übermittelt werden, wenn WMI mehr als fünf e-Mail-Ereignisse in dieser 300 Sekunden empfängt.</span><span class="sxs-lookup"><span data-stu-id="4486d-117">Also, the query requests the [**\_\_AggregateEvent**](--aggregateevent.md) instance should be delivered only if WMI receives more than five email events in that 300 seconds.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



<span data-ttu-id="4486d-118">Im folgenden Beispiel werden alle empfangenen Ereignisse in 600 Sekunden (d. h. 10 Minuten) von der **TargetInstance** gruppiert. **SourceName** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4486d-118">The following example groups all events received in 600 seconds (that is, 10 minutes) by the **TargetInstance**.**SourceName** property.</span></span> <span data-ttu-id="4486d-119">In diesem Beispiel werden Aggregat Ereignisse nur dann übermittelt, wenn die Anzahl der von derselben Quelle empfangenen [**Win32- \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) -Ereignisse 25 überschreitet.</span><span class="sxs-lookup"><span data-stu-id="4486d-119">In this example, aggregate events are delivered only if the number of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) events received from the same source exceeds 25.</span></span> <span data-ttu-id="4486d-120">Beachten Sie, dass der ISA-Operator bewirkt, dass die **TargetInstance** -Eigenschaft der [**\_ \_ instancecreationevent**](--instancecreationevent.md) -System Klasse eine Instanz der Win32-Klasse **\_ ntlogevent** darstellt.</span><span class="sxs-lookup"><span data-stu-id="4486d-120">Keep in mind that the ISA operator causes the **TargetInstance** property of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) system class to represent an instance of the **Win32\_NTLogEvent** class.</span></span>


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
