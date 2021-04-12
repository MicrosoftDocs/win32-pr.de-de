---
description: Beschreibt die grundlegende Syntax einer SELECT-Anweisung für Ereignis Abfragen.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: SELECT-Anweisung für Ereignis Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab840072269d04987bf42939f1f566ee6b99afab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217956"
---
# <a name="select-statement-for-event-queries"></a><span data-ttu-id="cf123-103">SELECT-Anweisung für Ereignis Abfragen</span><span class="sxs-lookup"><span data-stu-id="cf123-103">SELECT Statement for Event Queries</span></span>

<span data-ttu-id="cf123-104">Sie können eine Vielzahl von SELECT-Anweisungen verwenden, um Ereignis Informationen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="cf123-104">You can use a variety of SELECT statements to query for event information.</span></span> <span data-ttu-id="cf123-105">Die Anweisungen können einfache Anweisungen sein, oder Sie können restriktiver sein, um das Resultset einzugrenzen, das von der Abfrage zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cf123-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="cf123-106">Das folgende Beispiel ist eine einfache SELECT-Anweisung, die verwendet wird, um Ereignis Informationen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="cf123-106">The following example is a basic SELECT statement that is used to query for event information.</span></span>


```sql
SELECT * FROM EventClass
```



<span data-ttu-id="cf123-107">Wenn ein Consumer eine Abfrage übermittelt, ist es eine Anforderung, über alle Vorkommen des Ereignisses benachrichtigt zu werden, die von **EventClass** dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cf123-107">When a consumer submits a query, it is a request to be notified of all occurrences of the event represented by **EventClass**.</span></span> <span data-ttu-id="cf123-108">Diese Anforderung enthält eine Benachrichtigungs Anforderung zu allen Ereignis System-und nicht-Systemeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cf123-108">This request includes a request for notification about all of the event system and nonsystem properties.</span></span> <span data-ttu-id="cf123-109">Wenn ein Ereignis Anbieter eine Abfrage übermittelt, registriert er die Unterstützung für das Erstellen von Benachrichtigungen, wenn ein Ereignis auftritt, das von **EventClass** dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf123-109">When an event provider submits a query, it registers support for generating notifications when an event represented by **EventClass** occurs.</span></span>

<span data-ttu-id="cf123-110">Consumer können einzelne Eigenschaften anstelle des Sternchen ( \* ) in der SELECT-Anweisung angeben.</span><span class="sxs-lookup"><span data-stu-id="cf123-110">Consumers can specify individual properties instead of the asterisk (\*) in the SELECT statement.</span></span>

<span data-ttu-id="cf123-111">Im folgenden Beispiel wird gezeigt, wie bestimmte Eigenschaften abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="cf123-111">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



<span data-ttu-id="cf123-112">Allerdings werden alle Eigenschaften eines eingebetteten Objekts zurückgegeben, auch wenn die Abfrage eingebettete Objekteigenschaften angibt.</span><span class="sxs-lookup"><span data-stu-id="cf123-112">However, all of the properties of an embedded object are returned, even if the query specifies embedded object properties.</span></span>

<span data-ttu-id="cf123-113">Das folgende Beispiel zeigt zwei Abfragen, die dieselben Daten zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cf123-113">The following example shows two queries that return the same data.</span></span>


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



<span data-ttu-id="cf123-114">Wenn eine System Eigenschaft für eine bestimmte Abfrage nicht relevant ist, enthält Sie **null**.</span><span class="sxs-lookup"><span data-stu-id="cf123-114">If a system property is not relevant for a specific query, it contains **NULL**.</span></span> <span data-ttu-id="cf123-115">Beispielsweise ist der Wert der **\_ \_ RelPath** -System Eigenschaft für alle Ereignis Abfragen **null** .</span><span class="sxs-lookup"><span data-stu-id="cf123-115">For example, the value of the **\_\_RELPATH** system property is **NULL** for all event queries.</span></span>

<span data-ttu-id="cf123-116">Die folgenden Systemeigenschaften enthalten **null** für Ereignis Abfragen:</span><span class="sxs-lookup"><span data-stu-id="cf123-116">The following system properties contain **NULL** for event queries:</span></span>

<dl> <span data-ttu-id="cf123-117">\_\_Namespace</span><span class="sxs-lookup"><span data-stu-id="cf123-117">\_\_Namespace</span></span>  
<span data-ttu-id="cf123-118">\_\_ADS</span><span class="sxs-lookup"><span data-stu-id="cf123-118">\_\_Path</span></span>  
<span data-ttu-id="cf123-119">\_\_RelPath</span><span class="sxs-lookup"><span data-stu-id="cf123-119">\_\_RelPath</span></span>  
<span data-ttu-id="cf123-120">\_\_Servers</span><span class="sxs-lookup"><span data-stu-id="cf123-120">\_\_Server</span></span>  
</dl>

<span data-ttu-id="cf123-121">Weitere Informationen finden Sie unter [WMI-System Eigenschafts Referenz](wmi-system-properties.md).</span><span class="sxs-lookup"><span data-stu-id="cf123-121">For more information, see [WMI System Property Reference](wmi-system-properties.md).</span></span>

<span data-ttu-id="cf123-122">Alle Ereignis Abfragen können eine optionale [WHERE-Klausel](where-clause.md)enthalten, aber WHERE-Klauseln werden hauptsächlich von Consumern verwendet, um zusätzliche Filter anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cf123-122">All event queries can include an optional [WHERE clause](where-clause.md), but WHERE clauses are primarily used by consumers to specify additional filtering.</span></span> <span data-ttu-id="cf123-123">Es wird dringend empfohlen, dass Consumer immer eine WHERE-Klausel angeben.</span><span class="sxs-lookup"><span data-stu-id="cf123-123">It is strongly recommended that consumers always specify a WHERE clause.</span></span> <span data-ttu-id="cf123-124">Die Kosten einer komplexen Abfrage sind im Vergleich zu den Kosten für die Bereitstellung und Verarbeitung nicht benötigter Benachrichtigungen minimal.</span><span class="sxs-lookup"><span data-stu-id="cf123-124">The cost of a complex query is minimal compared to the cost of delivering and processing unneeded notifications.</span></span>

<span data-ttu-id="cf123-125">Das folgende Beispiel zeigt eine Abfrage, die Benachrichtigungen zu allen instanzänderungsereignissen anfordert, die die hypothetische Klasse **EmailEvent** betreffen.</span><span class="sxs-lookup"><span data-stu-id="cf123-125">The following example shows a query that requests notifications of all instance modification events that affect the hypothetical class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent
```



<span data-ttu-id="cf123-126">Wenn Ereignisse, die **EmailEvent** zugeordnet sind, häufig auftreten, wird der Consumer mit Ereignissen überflutet.</span><span class="sxs-lookup"><span data-stu-id="cf123-126">If events associated with **EmailEvent** occur frequently, the consumer is flooded with events.</span></span> <span data-ttu-id="cf123-127">Eine bessere Abfrage fordert Ereignisse nur dann an, wenn bestimmte Bedingungen Eigenschaften der angegebenen Klasse verwenden, z. b. wenn die Wichtigkeits Stufe hoch ist.</span><span class="sxs-lookup"><span data-stu-id="cf123-127">A better query requests events only when specific conditions use properties of the class specified, such as when the importance level is high.</span></span>

<span data-ttu-id="cf123-128">Das folgende Beispiel zeigt die Abfrage, die Sie verwenden können, wenn **emailimportance** eine Eigenschaft der Klasse **EmailEvent** ist.</span><span class="sxs-lookup"><span data-stu-id="cf123-128">The following example shows the query you can use if **EmailImportance** is a property of the class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



<span data-ttu-id="cf123-129">Beachten Sie, dass WMI eine Abfrage aus verschiedenen Gründen ablehnen kann.</span><span class="sxs-lookup"><span data-stu-id="cf123-129">Note that WMI can reject a query for a number of reasons.</span></span> <span data-ttu-id="cf123-130">Beispielsweise kann die Abfrage zu komplex oder für die Auswertung ressourcenintensiv sein.</span><span class="sxs-lookup"><span data-stu-id="cf123-130">For example, the query can be too complex or resource-intensive for evaluation.</span></span> <span data-ttu-id="cf123-131">In diesem Fall gibt WMI bestimmte Fehlercodes zurück, z. **b. \_ eine \_ ungültige \_ WBEM E-Abfrage**.</span><span class="sxs-lookup"><span data-stu-id="cf123-131">When this occurs, WMI returns specific error codes, such as **WBEM\_E\_INVALID\_QUERY**.</span></span>

<span data-ttu-id="cf123-132">Eigenschaften von eingebetteten Objekten können in der WHERE-Klausel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf123-132">Properties of embedded objects can be used in the WHERE clause.</span></span>

<span data-ttu-id="cf123-133">Im folgenden Beispiel wird gezeigt, wie Objekte abgefragt werden, bei denen die **TargetInstance** -Eigenschaft der System Klasse [**\_ \_ instancemodificationevent**](--instancemodificationevent.md) ein eingebettetes [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Objekt und **FreeSpace** eine Eigenschaft von **Win32 \_ LogicalDisk** ist.</span><span class="sxs-lookup"><span data-stu-id="cf123-133">The following example shows how to query for objects where the **TargetInstance** property of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system class is an embedded [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) object and **FreeSpace** is a property of **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a><span data-ttu-id="cf123-134">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf123-134">Examples</span></span>

<span data-ttu-id="cf123-135">Das [Überwachungs Erstellungs Ereignis für einen bestimmten Prozessnamen](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) VBScript-Beispiel auf TechNet verwendet die SELECT-Anweisung zum Überwachen von WMI-Instanzen Erstellungs Ereignissen für den Win32- \_ Prozess, Filtern nach einem bestimmten Prozessnamen.</span><span class="sxs-lookup"><span data-stu-id="cf123-135">The [Monitor creation event for specific process name](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) VBScript sample on TechNet uses the SELECT statement to monitor WMI instance creation events for Win32\_Process, filtering for a specific process name.</span></span>

 

 
