---
description: Verwenden Sie die WHERE-Klausel, um den Bereich einer Daten-, Ereignis- oder Schemaabfrage zu engen.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: WHERE-Klausel (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0587bffb1a10c4611773de8a61fdb7ac1576952
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386720"
---
# <a name="where-clause-wmi"></a><span data-ttu-id="49cab-103">WHERE-Klausel (WMI)</span><span class="sxs-lookup"><span data-stu-id="49cab-103">WHERE Clause (WMI)</span></span>

<span data-ttu-id="49cab-104">Verwenden Sie die WHERE-Klausel, um den Bereich einer Daten-, Ereignis- oder Schemaabfrage zu engen.</span><span class="sxs-lookup"><span data-stu-id="49cab-104">Use the WHERE clause to narrow the scope of a data, event, or schema query.</span></span> <span data-ttu-id="49cab-105">Weitere Informationen finden Sie unter [Abfragen mit WQL.](querying-with-wql.md)</span><span class="sxs-lookup"><span data-stu-id="49cab-105">For more information, see [Querying with WQL](querying-with-wql.md).</span></span> <span data-ttu-id="49cab-106">Die WHERE-Klausel besteht aus einer Eigenschaft oder einem Schlüsselwort, einem Operator und einer Konstante.</span><span class="sxs-lookup"><span data-stu-id="49cab-106">The WHERE clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="49cab-107">Alle WHERE-Klauseln müssen einen der vordefinierten Operatoren angeben, die in der Windows-Verwaltungsinstrumentation (WMI) Query Language (WQL) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="49cab-107">All WHERE clauses must specify one of the predefined operators that are included in the Windows Management Instrumentation (WMI) Query Language (WQL).</span></span> <span data-ttu-id="49cab-108">Sie können die WHERE-Klausel mit einer der folgenden Formen an die SELECT-Anweisung anfügen:</span><span class="sxs-lookup"><span data-stu-id="49cab-108">You can append the WHERE clause to the SELECT statement using one of the following forms:</span></span>


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



<span data-ttu-id="49cab-109">Wobei das abgefragte Element ist, ist class die Klasse, in der abgefragt werden soll, und constant, operator und property sind die Konstante, der Operator und die Eigenschaft oder das Schlüsselwort, die \* verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="49cab-109">where \* is the item queried about, class is the class in which to query, and constant, operator, and property are the constant, operator, and property or keyword to use.</span></span> <span data-ttu-id="49cab-110">Weitere Informationen zur SELECT-Anweisung finden Sie unter [SELECT-Anweisung](select-statement-for-data-queries.md)für Datenabfragen, [SELECT-Anweisung](select-statement-for-event-queries.md)für Ereignisabfragen oder [SELECT-Anweisung für Schemaabfragen.](select-statement-for-schema-queries.md)</span><span class="sxs-lookup"><span data-stu-id="49cab-110">For more information about the SELECT statement, see [SELECT Statement for Data Queries](select-statement-for-data-queries.md), [SELECT Statement for Event Queries](select-statement-for-event-queries.md), or [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="49cab-111">Der Wert der Konstante muss den richtigen Typ für die Eigenschaft haben.</span><span class="sxs-lookup"><span data-stu-id="49cab-111">The value of the constant must be of the correct type for the property.</span></span> <span data-ttu-id="49cab-112">Darüber hinaus muss der -Operator in der Liste der gültigen [WQL-Operatoren enthalten sein.](wql-operators.md)</span><span class="sxs-lookup"><span data-stu-id="49cab-112">Moreover, the operator must be among the list of valid [WQL operators](wql-operators.md).</span></span> <span data-ttu-id="49cab-113">Entweder ein Eigenschaftenname oder eine Konstante muss auf beiden Seiten des Operators in der WHERE-Klausel angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="49cab-113">Either a property name or a constant must appear on either side of the operator in the WHERE clause.</span></span>

<span data-ttu-id="49cab-114">Sie können Zeichenfolgenliterale wie "NTFS" in einer WHERE-Klausel verwenden.</span><span class="sxs-lookup"><span data-stu-id="49cab-114">You may use string literals, such as "NTFS", in a WHERE clause.</span></span> <span data-ttu-id="49cab-115">Wenn Sie die folgenden Sonderzeichen in die Zeichenfolge eingeben möchten, müssen Sie das Zeichen zunächst mit Escapezeichen verketten, indem Sie dem Zeichen einen zurückgestellten Schrägstrich ( ) voran \\ stellen:</span><span class="sxs-lookup"><span data-stu-id="49cab-115">If you wish to include the following special characters in your string, you must first escape the character by prefixing the character with a backslash (\\):</span></span>

-   <span data-ttu-id="49cab-116">schräger Schrägstrich ( \\ \\ )</span><span class="sxs-lookup"><span data-stu-id="49cab-116">backslash (\\\\)</span></span>
-   <span data-ttu-id="49cab-117">doppelte Anführungszeichen ( \\ ")</span><span class="sxs-lookup"><span data-stu-id="49cab-117">double quotes (\\")</span></span>
-   <span data-ttu-id="49cab-118">einfache Anführungszeichen ( \\ ')</span><span class="sxs-lookup"><span data-stu-id="49cab-118">single quotes (\\')</span></span>

<span data-ttu-id="49cab-119">Beliebige arithmetische Ausdrücke können nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49cab-119">Arbitrary arithmetic expressions cannot be used.</span></span> <span data-ttu-id="49cab-120">Die folgende Abfrage gibt beispielsweise nur die Instanzen der [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) zurück, die NTFS-Laufwerke darstellen:</span><span class="sxs-lookup"><span data-stu-id="49cab-120">For example, the following query returns only the instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class that represent NTFS drives:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



<span data-ttu-id="49cab-121">Eigenschaftsnamen können nicht auf beiden Seiten des Operators angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="49cab-121">Property names cannot appear on both sides of the operator.</span></span> <span data-ttu-id="49cab-122">Die folgende Abfrage ist ein Beispiel für eine ungültige Abfrage:</span><span class="sxs-lookup"><span data-stu-id="49cab-122">The following query is an example of an invalid query:</span></span>


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



<span data-ttu-id="49cab-123">Bei den meisten Verwendungen von Klassendeskriptoren in einer WHERE-Klausel kennzeichnet WMI die Abfrage als ungültig und gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="49cab-123">For most uses of class descriptors in a WHERE clause, WMI flags the query as invalid and returns an error.</span></span> <span data-ttu-id="49cab-124">Verwenden Sie jedoch den Punktoperator (.) für Eigenschaften vom Typ **Objekt** in WMI.</span><span class="sxs-lookup"><span data-stu-id="49cab-124">However, use the dot (.) operator for properties of type **object** in WMI.</span></span> <span data-ttu-id="49cab-125">Die folgende Abfrage ist beispielsweise gültig, wenn Prop eine gültige Eigenschaft von MyClass und ein Typobjekt **ist:**</span><span class="sxs-lookup"><span data-stu-id="49cab-125">For example, the following query is valid if Prop is a valid property of MyClass and is type **object**:</span></span>

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

<span data-ttu-id="49cab-126">Bei Vergleichstests wird die Groß-/Kleinschreibung immer nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="49cab-126">Comparison tests are always case-insensitive.</span></span> <span data-ttu-id="49cab-127">Das heißt, die folgenden drei Anweisungen werden alle als **TRUE ausgewertet:**</span><span class="sxs-lookup"><span data-stu-id="49cab-127">That is, the following three statements all evaluate to **TRUE**:</span></span>


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



<span data-ttu-id="49cab-128">Sie können eine Abfrage erstellen, die boolesche Datentypen enthält, aber die einzigen gültigen booleschen Operandentypen sind die Typen =, != und <> .</span><span class="sxs-lookup"><span data-stu-id="49cab-128">You can construct a query that includes Boolean data types, but the only valid Boolean operand types are the =, != and <> types.</span></span> <span data-ttu-id="49cab-129">Der Wert **TRUE** entspricht der Zahl 1, und der Wert **FALSE** entspricht der Zahl 0.</span><span class="sxs-lookup"><span data-stu-id="49cab-129">The value **TRUE** is equivalent to the number 1, and the value **FALSE** is equivalent to the number 0.</span></span> <span data-ttu-id="49cab-130">Die folgenden Beispiele sind Abfragen, die einen booleschen Wert mit den Werten **TRUE** oder **FALSE vergleichen.**</span><span class="sxs-lookup"><span data-stu-id="49cab-130">The following examples are of queries that compare a Boolean value against the values **TRUE** or **FALSE**.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp = 1
SELECT * FROM MyClass WHERE BoolProp = TRUE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
SELECT * FROM MyClass WHERE BoolProp = 0
SELECT * FROM MyClass WHERE BoolProp = FALSE
SELECT * FROM MyClass WHERE BoolProp != 1
SELECT * FROM MyClass WHERE BoolProp != FALSE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
```



<span data-ttu-id="49cab-131">Die folgenden Beispiele sind ungültige Abfragen, die versuchen, ungültige Operanden zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="49cab-131">The following examples are of invalid queries that attempt to use invalid operands.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



<span data-ttu-id="49cab-132">Mehrere Gruppen von Eigenschaften, Operatoren und Konstanten können in einer WHERE-Klausel mithilfe logischer Operatoren und klammerischer Teilausdrucke kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="49cab-132">Multiple groups of properties, operators, and constants can be combined in a WHERE clause using logical operators and parenthetical subexpressions.</span></span> <span data-ttu-id="49cab-133">Jede Gruppe muss mit den Operatoren AND, OR oder [NOT](wql-operators.md) verbunden werden, wie in den folgenden Abfragen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="49cab-133">Each group must be joined with the AND, OR, or NOT [operators](wql-operators.md) as is shown in the following queries.</span></span> <span data-ttu-id="49cab-134">Die erste Abfrage ruft alle Instanzen der [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) ab, bei der die **Name-Eigenschaft** entweder auf C oder D festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="49cab-134">The first query retrieves all instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class with the **Name** property set to either C or D:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



<span data-ttu-id="49cab-135">Die zweite Abfrage ruft Datenträger mit den Namen "C:" oder "D:" nur dann ab, wenn sie über eine bestimmte Menge an freiem Speicherplatz und NTFS-Dateisystemen verfügen:</span><span class="sxs-lookup"><span data-stu-id="49cab-135">The second query retrieves disks named "C:" or "D:" only if they have a certain amount of free space remaining and have NTFS file systems:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



<span data-ttu-id="49cab-136">Dieses Beispiel zeigt eine Schemaabfrage mithilfe der WHERE-Klausel.</span><span class="sxs-lookup"><span data-stu-id="49cab-136">This example shows a schema query using the WHERE clause.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



<span data-ttu-id="49cab-137">Die Klassenmetaklasse identifiziert dies als Schemaabfrage, die Eigenschaft namens this identifiziert die Zielklasse der Abfrage, und der ISA-Operator fordert Definitionen für die Unterklassen der \_ \_ \_ Zielklasse an. [](isa-operator-for-schema-queries.md)</span><span class="sxs-lookup"><span data-stu-id="49cab-137">The class meta\_class identifies this as a schema query, the property called \_\_this identifies the target class of the query and the [ISA operator](isa-operator-for-schema-queries.md) requests definitions for the subclasses of the target class.</span></span> <span data-ttu-id="49cab-138">Daher gibt die vorherige Abfrage die Definition für die myClassName-Klasse und Definitionen für alle ihre Unterklassen zurück.</span><span class="sxs-lookup"><span data-stu-id="49cab-138">Therefore, the preceding query returns the definition for the myClassName class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="49cab-139">Das folgende Beispiel ist eine Datenabfrage, die die [ASSOCIATORS OF-Anweisung mit](associators-of-statement.md) WHERE verwendet:</span><span class="sxs-lookup"><span data-stu-id="49cab-139">The following example is a data query using the [ASSOCIATORS OF statement](associators-of-statement.md) with WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



<span data-ttu-id="49cab-140">Das nächste Beispiel zeigt eine Schemaabfrage mit ASSOCIATORS OF und WHERE:</span><span class="sxs-lookup"><span data-stu-id="49cab-140">The next example shows a schema query using ASSOCIATORS OF and WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="49cab-141">Das folgende Beispiel ist eine Datenabfrage, die die [REFERENCES OF-Anweisung und](references-of-statement.md) WHERE verwendet:</span><span class="sxs-lookup"><span data-stu-id="49cab-141">The following example is a data query using the [REFERENCES OF statement](references-of-statement.md) and WHERE:</span></span>


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



<span data-ttu-id="49cab-142">Das letzte Beispiel ist eine Schemaabfrage mit REFERENCES OF und WHERE:</span><span class="sxs-lookup"><span data-stu-id="49cab-142">This last example is a schema query using REFERENCES OF and WHERE:</span></span>


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="49cab-143">Zusätzlich zum WMI [DATETIME-Format](date-and-time-format.md) unterstützt die WQL WHERE-Klausel mehrere andere Datums- und Uhrzeitformate:</span><span class="sxs-lookup"><span data-stu-id="49cab-143">In addition to the WMI [DATETIME](date-and-time-format.md) format, the WQL WHERE clause supports several other date and time formats:</span></span>

-   [<span data-ttu-id="49cab-144">Von WQL unterstützte Datumsformate</span><span class="sxs-lookup"><span data-stu-id="49cab-144">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
-   [<span data-ttu-id="49cab-145">Von WQL unterstützte Zeitformate</span><span class="sxs-lookup"><span data-stu-id="49cab-145">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)

 

 
