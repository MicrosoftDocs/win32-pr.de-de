---
description: Der WMI Query Language (WQL) ist eine Teilmenge der American National Standards Institute Structured Query Language (ANSI SQL) &\# 8212; mit geringfügigen Semantik Änderungen. In der folgenden Tabelle werden die WQL-Schlüsselwörter aufgelistet.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (WMI SQL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87498b6e8e37ab900e21eedf2c15d5cdba9f9bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215438"
---
# <a name="wql-sql-for-wmi"></a><span data-ttu-id="15ba2-104">WQL (WMI SQL)</span><span class="sxs-lookup"><span data-stu-id="15ba2-104">WQL (SQL for WMI)</span></span>

<span data-ttu-id="15ba2-105">Der WMI Query Language (WQL) ist eine Teilmenge der American National Standards Institute Structured Query Language (ANSI SQL) mit geringfügigen Semantik Änderungen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-105">The WMI Query Language (WQL) is a subset of the American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes.</span></span> <span data-ttu-id="15ba2-106">In der folgenden Tabelle werden die WQL-Schlüsselwörter aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="15ba2-106">The following table lists the WQL keywords.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15ba2-107">WQL-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="15ba2-107">WQL keyword</span></span></th>
<th><span data-ttu-id="15ba2-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="15ba2-108">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15ba2-109">AND</span><span class="sxs-lookup"><span data-stu-id="15ba2-109">AND</span></span><br/></td>
<td><span data-ttu-id="15ba2-110">Kombiniert zwei boolesche Ausdrücke und gibt <strong>true</strong> zurück, wenn beide Ausdrücke <strong>true</strong>sind.</span><span class="sxs-lookup"><span data-stu-id="15ba2-110">Combines two Boolean expressions, and returns <strong>TRUE</strong> when both expressions are <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15ba2-111"><a href="associators-of-statement.md">assoziatoren von</a></span><span class="sxs-lookup"><span data-stu-id="15ba2-111"><a href="associators-of-statement.md">ASSOCIATORS OF</a></span></span></td>
<td><span data-ttu-id="15ba2-112">Ruft alle-Instanzen ab, die einer-Quell Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="15ba2-112">Retrieves all instances that are associated with a source instance.</span></span><br/> <span data-ttu-id="15ba2-113">Verwenden Sie diese Anweisung mit Schema Abfragen und Daten Abfragen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-113">Use this statement with schema queries and data queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15ba2-114"><a href="--class-identifier.md">__CLASS</a></span><span class="sxs-lookup"><span data-stu-id="15ba2-114"><a href="--class-identifier.md">__CLASS</a></span></span></td>
<td><span data-ttu-id="15ba2-115">Verweist auf die-Klasse des-Objekts in einer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="15ba2-115">References the class of the object in a query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15ba2-116">FROM</span><span class="sxs-lookup"><span data-stu-id="15ba2-116">FROM</span></span><br/></td>
<td><span data-ttu-id="15ba2-117">Gibt die Klasse an, die die in einer SELECT-Anweisung aufgeführten Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="15ba2-117">Specifies the class that contains the properties listed in a SELECT statement.</span></span> <span data-ttu-id="15ba2-118">Windows-Verwaltungsinstrumentation (WMI) unterstützt Daten Abfragen von nur einer Klasse gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="15ba2-118">Windows Management Instrumentation (WMI) supports data queries from only one class at a time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15ba2-119"><a href="group-clause.md">Group-Klausel</a></span><span class="sxs-lookup"><span data-stu-id="15ba2-119"><a href="group-clause.md">GROUP Clause</a></span></span></td>
<td><span data-ttu-id="15ba2-120">Bewirkt, dass WMI eine Benachrichtigung generiert, um eine Gruppe von Ereignissen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-120">Causes WMI to generate one notification to represent a group of events.</span></span><br/> <span data-ttu-id="15ba2-121">Verwenden Sie diese Klausel mit Ereignis Abfragen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-121">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15ba2-122"><a href="having-clause.md">HAVING</a></span><span class="sxs-lookup"><span data-stu-id="15ba2-122"><a href="having-clause.md">HAVING</a></span></span></td>
<td><span data-ttu-id="15ba2-123">Filtert die Ereignisse, die während des in der <a href="within-clause.md">within-Klausel</a>angegebenen Gruppierungs Intervalls empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="15ba2-123">Filters the events that are received during the grouping interval that is specified in the <a href="within-clause.md">WITHIN clause</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15ba2-124"><a href="wql-operators.md">IS</a></span><span class="sxs-lookup"><span data-stu-id="15ba2-124"><a href="wql-operators.md">IS</a></span></span></td>
<td><span data-ttu-id="15ba2-125">Vergleichs Operator, der mit Not und <strong>null</strong>verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="15ba2-125">Comparison operator used with NOT and <strong>NULL</strong>.</span></span> <span data-ttu-id="15ba2-126">Die Syntax für diese Anweisung lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="15ba2-126">The syntax for this statement is the following:</span></span><br/> <span data-ttu-id="15ba2-127">ist [NOT] <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="15ba2-127">IS [NOT] <strong>NULL</strong></span></span><br/> <span data-ttu-id="15ba2-128">(wobei nicht optional ist)</span><span class="sxs-lookup"><span data-stu-id="15ba2-128">(where NOT is optional)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15ba2-129"><a href="wql-operators.md">ISA</a></span><span class="sxs-lookup"><span data-stu-id="15ba2-129"><a href="wql-operators.md">ISA</a></span></span></td>
<td><span data-ttu-id="15ba2-130">Operator, der eine Abfrage auf die Unterklassen einer angegebenen Klasse anwendet.</span><span class="sxs-lookup"><span data-stu-id="15ba2-130">Operator that applies a query to the subclasses of a specified class.</span></span> <span data-ttu-id="15ba2-131">Weitere Informationen finden Sie unter <a href="isa-operator-for-event-queries.md">ISA-Operator für Ereignis Abfragen</a>, <a href="isa-operator-for-data-queries.md">ISA-Operator für Daten Abfragen</a>und <a href="isa-operator-for-schema-queries.md">ISA-Operator für Schema Abfragen</a>.</span><span class="sxs-lookup"><span data-stu-id="15ba2-131">For more information, see <a href="isa-operator-for-event-queries.md">ISA Operator for Event Queries</a>, <a href="isa-operator-for-data-queries.md">ISA Operator for Data Queries</a>, and <a href="isa-operator-for-schema-queries.md">ISA Operator for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15ba2-132">Keysonly</span><span class="sxs-lookup"><span data-stu-id="15ba2-132">KEYSONLY</span></span><br/></td>
<td><span data-ttu-id="15ba2-133">Wird in <a href="references-of-statement.md">verweisen von</a> und <a href="associators-of-statement.md">assoziatoren von</a> Abfragen verwendet, um sicherzustellen, dass die resultierenden Instanzen nur mit den Schlüsseln der-Instanzen aufgefüllt werden, wodurch der Aufwand des Aufrufes verringert wird.</span><span class="sxs-lookup"><span data-stu-id="15ba2-133">Used in <a href="references-of-statement.md">REFERENCES OF</a> and <a href="associators-of-statement.md">ASSOCIATORS OF</a> queries to ensure that the resulting instances are only populated with the keys of the instances, which reduces the overhead of the call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15ba2-134"><a href="wql-operators.md">LIKE</a></span><span class="sxs-lookup"><span data-stu-id="15ba2-134"><a href="wql-operators.md">LIKE</a></span></span></td>
<td><span data-ttu-id="15ba2-135">Operator, der bestimmt, ob eine angegebene Zeichenfolge mit einem angegebenen Muster übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="15ba2-135">Operator that determines whether or not a given character string matches a specified pattern.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15ba2-136">NICHT</span><span class="sxs-lookup"><span data-stu-id="15ba2-136">NOT</span></span><br/></td>
<td><span data-ttu-id="15ba2-137">Vergleichs Operator, der in einer WQL SELECT-Abfrage verwendet, z. b.:</span><span class="sxs-lookup"><span data-stu-id="15ba2-137">Comparison operator that use in a WQL SELECT query, for example:</span></span><br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15ba2-138"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="15ba2-138"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="15ba2-139">Gibt an, dass ein Objekt über keinen explizit zugewiesenen Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="15ba2-139">Indicates an object does not have an explicitly assigned value.</span></span> <span data-ttu-id="15ba2-140"><strong>Null</strong> entspricht nicht 0 (null) oder leer.</span><span class="sxs-lookup"><span data-stu-id="15ba2-140"><strong>NULL</strong> is not equivalent to zero (0) or blank.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15ba2-141">oder</span><span class="sxs-lookup"><span data-stu-id="15ba2-141">OR</span></span><br/></td>
<td><span data-ttu-id="15ba2-142">Kombiniert zwei Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-142">Combines two conditions.</span></span><br/> <span data-ttu-id="15ba2-143">Wenn mehr als ein logischer Operator in einer-Anweisung verwendet wird, werden die-oder-Operatoren nach den Operatoren und ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="15ba2-143">When more than one logical operator is used in a statement, the OR operators are evaluated after the AND operators.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15ba2-144"><a href="references-of-statement.md">Verweise auf</a></span><span class="sxs-lookup"><span data-stu-id="15ba2-144"><a href="references-of-statement.md">REFERENCES OF</a></span></span></td>
<td><span data-ttu-id="15ba2-145">Ruft alle Assoziations Instanzen ab, die auf eine bestimmte Quell Instanz verweisen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-145">Retrieves all association instances that refer to a specific source instance.</span></span> <span data-ttu-id="15ba2-146">Verwenden Sie diese Anweisung mit Schema-und Daten Abfragen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-146">Use this statement with schema and data queries.</span></span> <span data-ttu-id="15ba2-147">Die <a href="references-of-statement.md">References of</a> -Anweisung ähnelt den <a href="associators-of-statement.md">assoziatoren der</a> -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="15ba2-147">The <a href="references-of-statement.md">REFERENCES OF</a> statement is similar to the <a href="associators-of-statement.md">ASSOCIATORS OF</a> statement.</span></span> <span data-ttu-id="15ba2-148">Endpunkt Instanzen werden jedoch nicht abgerufen. die Zuordnungs Instanzen werden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-148">However, it does not retrieve endpoint instances; it retrieves the association instances.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15ba2-149">SELECT</span><span class="sxs-lookup"><span data-stu-id="15ba2-149">SELECT</span></span><br/></td>
<td><span data-ttu-id="15ba2-150">Gibt die Eigenschaften an, die in einer Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15ba2-150">Specifies the properties that are used in a query.</span></span><br/> <span data-ttu-id="15ba2-151">Weitere Informationen finden Sie unter <a href="select-statement-for-data-queries.md">SELECT-Anweisung für Daten Abfragen</a>, <a href="select-statement-for-event-queries.md">SELECT-Anweisung für Ereignis Abfragen</a>oder <a href="select-statement-for-schema-queries.md">SELECT-Anweisung für Schema Abfragen</a>.</span><span class="sxs-lookup"><span data-stu-id="15ba2-151">For more information, see <a href="select-statement-for-data-queries.md">SELECT Statement for Data Queries</a>, <a href="select-statement-for-event-queries.md">SELECT Statement for Event Queries</a>, or <a href="select-statement-for-schema-queries.md">SELECT Statement for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15ba2-152"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="15ba2-152"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="15ba2-153">Boolescher Operator, der ergibt-1 (minus 1).</span><span class="sxs-lookup"><span data-stu-id="15ba2-153">Boolean operator that evaluates to -1 (minus one).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15ba2-154"><a href="where-clause.md">WHERE</a></span><span class="sxs-lookup"><span data-stu-id="15ba2-154"><a href="where-clause.md">WHERE</a></span></span></td>
<td><span data-ttu-id="15ba2-155">Schränkt den Gültigkeitsbereich einer Daten-, Ereignis-oder Schema Abfrage ein.</span><span class="sxs-lookup"><span data-stu-id="15ba2-155">Narrows the scope of a data, event, or schema query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15ba2-156"><a href="within-clause.md">WITHIN</a></span><span class="sxs-lookup"><span data-stu-id="15ba2-156"><a href="within-clause.md">WITHIN</a></span></span></td>
<td><span data-ttu-id="15ba2-157">Gibt ein Abruf-oder Gruppierungs Intervall an.</span><span class="sxs-lookup"><span data-stu-id="15ba2-157">Specifies a polling or grouping interval.</span></span><br/> <span data-ttu-id="15ba2-158">Verwenden Sie diese Klausel mit Ereignis Abfragen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-158">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15ba2-159">false</span><span class="sxs-lookup"><span data-stu-id="15ba2-159">FALSE</span></span><br/></td>
<td><span data-ttu-id="15ba2-160">Boolescher Operator, der als 0 (null) ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="15ba2-160">Boolean operator that evaluates to 0 (zero).</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="15ba2-161">Wenn Sie ein WQL-Schlüsselwort als Objektnamen verwenden, kann dies zu einer Abfrage führen, die auch dann nicht analysiert werden kann, wenn die Abfrage ohne Fehler kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="15ba2-161">Using a WQL key word as an object name can result in a query that cannot be parsed even when the query compiles without error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="15ba2-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15ba2-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15ba2-163">WQL-Operatoren</span><span class="sxs-lookup"><span data-stu-id="15ba2-163">WQL Operators</span></span>](wql-operators.md)
</dt> <dt>

[<span data-ttu-id="15ba2-164">WQL-unterstützte Datumsformate</span><span class="sxs-lookup"><span data-stu-id="15ba2-164">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
</dt> <dt>

[<span data-ttu-id="15ba2-165">Von WQL unterstützte Zeitformate</span><span class="sxs-lookup"><span data-stu-id="15ba2-165">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)
</dt> </dl>

 

 




