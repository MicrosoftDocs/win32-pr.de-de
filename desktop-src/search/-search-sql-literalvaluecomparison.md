---
description: Der literale Wert Vergleich verwendet Standard Vergleichs Operatoren, um eine einwertige Spalte mit einem Literalwert zu vergleichen.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Vergleich von literalen Werten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8577e5a97dcc92131658c325f175efa1d0c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346909"
---
# <a name="literal-value-comparison"></a><span data-ttu-id="96ffe-103">Vergleich von literalen Werten</span><span class="sxs-lookup"><span data-stu-id="96ffe-103">Literal Value Comparison</span></span>

<span data-ttu-id="96ffe-104">Der literale Wert Vergleich verwendet Standard Vergleichs Operatoren, um eine einwertige Spalte mit einem [Literalwert](-search-sql-literals.md) zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="96ffe-104">The literal value comparison uses standard comparison operators for matching a single-valued column to a [literal](-search-sql-literals.md) value.</span></span> <span data-ttu-id="96ffe-105">Weitere Informationen zum Vergleichen von mehrwertigen Spalten finden Sie unter [Vergleiche mit mehreren Werten (Array)](-search-sql-multivaluedcomparisons.md).</span><span class="sxs-lookup"><span data-stu-id="96ffe-105">For information about comparing multivalued columns, see [Multi-Valued (ARRAY) Comparisons](-search-sql-multivaluedcomparisons.md).</span></span>

<span data-ttu-id="96ffe-106">Das Vergleichs Prädikat literale Wert weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="96ffe-106">The literal value comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> <span data-ttu-id="96ffe-107">Die Rechte Seite des Vergleichs muss ein Literalwert sein.</span><span class="sxs-lookup"><span data-stu-id="96ffe-107">The right side of the comparison must be a literal.</span></span> <span data-ttu-id="96ffe-108">Es ist nicht möglich, eine Spalte mit einem berechneten Wert zu vergleichen, und Sie können eine Spalte nicht mit einer anderen Spalte vergleichen.</span><span class="sxs-lookup"><span data-stu-id="96ffe-108">You cannot compare a column against a computed value, and you cannot compare a column against another column.</span></span>

 

<span data-ttu-id="96ffe-109">Der Spalten Teil ist eine beliebige gültige Eigenschafts Spalte und kann ggf. in einen anderen Typ umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="96ffe-109">The column part is any valid property column and can be cast to another type if necessary.</span></span> <span data-ttu-id="96ffe-110">Optional können Sie den Spaltennamen für die Lesbarkeit in doppelte Anführungszeichen einschließen, ohne dass sich dies auf die Funktionalität auswirkt.</span><span class="sxs-lookup"><span data-stu-id="96ffe-110">Optionally, you can enclose the column name in double quotes for readability without affecting functionality.</span></span> <span data-ttu-id="96ffe-111">Weitere Informationen finden Sie unter umwandeln [des Datentyps einer Spalte](-search-sql-castingdatacolumntype.md).</span><span class="sxs-lookup"><span data-stu-id="96ffe-111">For more information, see [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

<span data-ttu-id="96ffe-112">Das Literale kann eine beliebige Zeichenfolge, ein numerisches, ein hexadezimal, ein boolescher Wert oder ein Datumsliteral in einfachen Anführungszeichen sein</span><span class="sxs-lookup"><span data-stu-id="96ffe-112">The literal can be any string, numeric, hexadecimal, Boolean, or date literal, enclosed in single quotation marks.</span></span> <span data-ttu-id="96ffe-113">Nur genaue Übereinstimmungen werden erkannt, und Platzhalter Zeichen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="96ffe-113">Only exact matches are recognized, and wildcard characters are ignored.</span></span> <span data-ttu-id="96ffe-114">Das Literale kann auch in einen anderen Typ umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="96ffe-114">The literal can also be cast to another type.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="96ffe-115">Vergleichsoperatoren</span><span class="sxs-lookup"><span data-stu-id="96ffe-115">Comparison Operators</span></span>

<span data-ttu-id="96ffe-116">In der folgenden Tabelle werden die unterstützten Vergleichs Operatoren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="96ffe-116">The following table describes the supported comparison operators.</span></span>



| <span data-ttu-id="96ffe-117">Vergleichsoperator</span><span class="sxs-lookup"><span data-stu-id="96ffe-117">Comparison operator</span></span> | <span data-ttu-id="96ffe-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96ffe-118">Description</span></span>              |
|---------------------|--------------------------|
| =                   | <span data-ttu-id="96ffe-119">Gleich</span><span class="sxs-lookup"><span data-stu-id="96ffe-119">Equal to</span></span>                 |
| <span data-ttu-id="96ffe-120">! = oder <></span><span class="sxs-lookup"><span data-stu-id="96ffe-120">!= or <></span></span>      | <span data-ttu-id="96ffe-121">Ungleich</span><span class="sxs-lookup"><span data-stu-id="96ffe-121">Not equal to</span></span>             |
| >                | <span data-ttu-id="96ffe-122">Größer als</span><span class="sxs-lookup"><span data-stu-id="96ffe-122">Greater than</span></span>             |
| >=               | <span data-ttu-id="96ffe-123">Größer als oder gleich</span><span class="sxs-lookup"><span data-stu-id="96ffe-123">Greater than or equal to</span></span> |
| <                | <span data-ttu-id="96ffe-124">Kleiner als</span><span class="sxs-lookup"><span data-stu-id="96ffe-124">Less than</span></span>                |
| <=               | <span data-ttu-id="96ffe-125">Kleiner als oder gleich</span><span class="sxs-lookup"><span data-stu-id="96ffe-125">Less than or equal to</span></span>    |



 

 

<span data-ttu-id="96ffe-126">In Verbindung mit dem Operator "=" unterstützt Windows Search Structured Query Language (SQL) die Verwendung der Schlüsselwörter "Before" und "After", die angeben, ob die Abfrage Spaltenwerte vor oder nach einem angegebenen Wert in der Wörterbuch Sortierung vergleichen soll.</span><span class="sxs-lookup"><span data-stu-id="96ffe-126">In conjunction with the "=" operator, Windows Search Structured Query Language (SQL) supports the use of BEFORE and AFTER keywords, which specify whether the query should compare column values before or after a specified value, in dictionary sort ordering.</span></span>


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a><span data-ttu-id="96ffe-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96ffe-127">Examples</span></span>

<span data-ttu-id="96ffe-128">Im folgenden finden Sie Beispiele für das Vergleichs Prädikat Literalwert.</span><span class="sxs-lookup"><span data-stu-id="96ffe-128">The following are examples of the literal value comparison predicate.</span></span>


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a><span data-ttu-id="96ffe-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="96ffe-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="96ffe-130">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="96ffe-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="96ffe-131">LIKE-Prädikat</span><span class="sxs-lookup"><span data-stu-id="96ffe-131">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="96ffe-132">DateAdd-Funktion</span><span class="sxs-lookup"><span data-stu-id="96ffe-132">DATEADD Function</span></span>](-search-sql-dateadd.md)
</dt> <dt>

[<span data-ttu-id="96ffe-133">Mehrwertige Vergleiche (Array)</span><span class="sxs-lookup"><span data-stu-id="96ffe-133">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="96ffe-134">NULL-Prädikat</span><span class="sxs-lookup"><span data-stu-id="96ffe-134">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="96ffe-135">**Licher**</span><span class="sxs-lookup"><span data-stu-id="96ffe-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="96ffe-136">Voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="96ffe-136">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="96ffe-137">Nicht-voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="96ffe-137">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



