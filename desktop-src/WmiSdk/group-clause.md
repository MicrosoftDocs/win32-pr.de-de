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
# <a name="group-clause"></a><span data-ttu-id="9f4ff-103">Group-Klausel</span><span class="sxs-lookup"><span data-stu-id="9f4ff-103">GROUP Clause</span></span>

<span data-ttu-id="9f4ff-104">Die Group-Klausel bewirkt, dass WMI eine einzelne Benachrichtigung generiert, um eine Gruppe von Ereignissen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-104">The GROUP clause causes WMI to generate a single notification to represent a group of events.</span></span> <span data-ttu-id="9f4ff-105">Die repräsentative Benachrichtigung ist eine Instanz der System Klasse [**\_ \_ aggregateevent**](--aggregateevent.md) .</span><span class="sxs-lookup"><span data-stu-id="9f4ff-105">The representative notification is an instance of the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span> <span data-ttu-id="9f4ff-106">Die **\_ \_ aggregateevent** -System Klasse enthält zwei Eigenschaften: " **repräsentativ** " und " **numofevents**".</span><span class="sxs-lookup"><span data-stu-id="9f4ff-106">The **\_\_AggregateEvent** system class contains two properties: **Representative** and **NumberOfEvents**.</span></span> <span data-ttu-id="9f4ff-107">Die **repräsentative** Eigenschaft ist ein eingebettetes Objekt, das eine der-Instanzen enthält, die während des in der [within-Klausel](within-clause.md)angegebenen Gruppierungs Intervalls empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-107">The **Representative** property is an embedded object that contains one of the instances received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="9f4ff-108">Wenn z. b. ein Aggregat Ereignis generiert wird, um über instanzänderungsereignisse zu benachrichtigen, enthält der **repräsentative** eine Instanz der [**\_ \_ instancemodificationevent**](--instancemodificationevent.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-108">For example, if an aggregate event is generated to notify of instance modification events, **Representative** contains one instance of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) class.</span></span> <span data-ttu-id="9f4ff-109">Die Eigenschaft " **numofevents** " enthält die Anzahl der Ereignisse, die während des Gruppierungs Intervalls empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-109">The **NumberOfEvents** property contains the number of events received during the grouping interval.</span></span> <span data-ttu-id="9f4ff-110">Das Gruppierungs Intervall gibt den Zeitraum an, nach dem ein erstes Ereignis empfangen wird, in dem WMI ähnliche Ereignisse erfassen sollte.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-110">The grouping interval specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span>

<span data-ttu-id="9f4ff-111">Die Group-Klausel muss eine within-Klausel enthalten, um das Gruppierungs Intervall anzugeben, und kann das-oder das-Schlüsselwort oder beides enthalten.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-111">The GROUP clause must contain a WITHIN clause to specify the grouping interval and can contain the BY or HAVING keyword, or both.</span></span> <span data-ttu-id="9f4ff-112">Die Group-Klausel wird nach der WHERE-Klausel eingefügt, wie im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="9f4ff-112">The GROUP clause is placed after the WHERE clause, as shown following:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

<span data-ttu-id="9f4ff-113">Der *EventClass* -Wert ist die Ereignisklasse, deren Member das Ereignis ist, und *value* ist der Wert für die Eigenschaft, für die eine Benachrichtigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-113">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="9f4ff-114">Das Intervall ist eine Ganzzahl ohne Vorzeichen, die das Gruppierungs Intervall nach dem Empfang des ersten Ereignisses darstellt.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-114">The interval is an unsigned integer that represents the grouping interval after receiving the first event.</span></span> <span data-ttu-id="9f4ff-115">Die ganze Zahl ohne Vorzeichen ist eine Anzahl von Sekunden.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-115">The unsigned integer is a number of seconds.</span></span> <span data-ttu-id="9f4ff-116">Die Eigenschaften Liste ist eine durch Trennzeichen getrennte Liste von mindestens einer Eigenschaft, die in der Ereignisklasse enthalten ist. der *Operator* ist ein beliebiger relationaler Operator. und *Integer* ist eine Ganzzahl ohne Vorzeichen, die eine ganze Zahl 32 ohne Vorzeichen angibt und eine Anzahl von Ereignissen angibt.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-116">The property list is a comma-delimited list of one or more properties that are included in the event class; *operator* is any relational operator; and *integer* is an unsigned 32-bit integer indicating a number of events.</span></span>

<span data-ttu-id="9f4ff-117">Wenn die Group-Klausel verwendet wird, sind die WHERE-, by-und have-Klauseln optional.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-117">When using the GROUP clause, the WHERE, BY, and HAVING clauses are optional.</span></span>

<span data-ttu-id="9f4ff-118">Eine grundlegende Verwendung der Group-Klausel kann eine Gruppierung von Ereignissen innerhalb eines Zeitintervalls anfordern, das beginnt, wenn das erste Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-118">A basic use of the GROUP clause might request a grouping of events within a time interval that starts when the first event is received.</span></span> <span data-ttu-id="9f4ff-119">Beispielsweise werden in der folgenden Abfrage alle e-Mail-Ereignisse, die innerhalb von fünf Minuten gesendet werden, gruppiert.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-119">For example, the following query groups all of the email events sent within 5 minutes.</span></span> <span data-ttu-id="9f4ff-120">Anstatt einen Benutzer jedes Mal, wenn eine neue e-Mail empfangen wird, zu Paging, kann der permanente Consumer diese Abfrage verwenden, um den Benutzer nur dann zu benachrichtigen, wenn innerhalb der letzten 5 Minuten eine neue e-Mail eingegangen ist.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-120">Instead of paging a user every time a piece of new email is received, the permanent consumer might use this query to inform the user only if new email has been received within the last 5 minutes.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



<span data-ttu-id="9f4ff-121">Wenn ausführlichere Informationen erforderlich sind, können Ereignisse nach einer oder mehreren Eigenschaften der Ereignisklasse gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-121">If more detailed information is required, events can be grouped by one or more properties of the event class.</span></span> <span data-ttu-id="9f4ff-122">Die folgende Abfrage fordert an, dass e-Mail-Ereignisse mit anderen Ereignissen kombiniert werden, die in der **Sender** -Eigenschaft denselben Wert aufweisen:</span><span class="sxs-lookup"><span data-stu-id="9f4ff-122">The following query requests that email events be combined with other events that have the same value in the **Sender** property:</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



<span data-ttu-id="9f4ff-123">Eine noch umfassendere Detailebene kann durch Hinzufügen einer WHERE-Klausel erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="9f4ff-123">A still greater level of detail can be achieved by adding a WHERE clause.</span></span> <span data-ttu-id="9f4ff-124">Die folgende Abfrage benachrichtigt z. b. einen Benutzer über neue e-Mails von einem bestimmten Absender, der innerhalb der letzten 10 Minuten eingetroffen ist, zusammen mit anderen Ereignissen, die in der **Wichtigkeits** Eigenschaft denselben Wert aufweisen:</span><span class="sxs-lookup"><span data-stu-id="9f4ff-124">For example, the following query notifies a user of new email from a particular sender that has arrived within the last 10 minutes, combined with other events that have the same value in the **Importance** property:</span></span>


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



