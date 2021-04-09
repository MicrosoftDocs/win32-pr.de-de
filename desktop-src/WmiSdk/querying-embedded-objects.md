---
description: Es gibt mehrere Möglichkeiten, wie eine Abfrage eine Abfrage durchführt, wenn eine Ereignisklasse abgefragt wird, die eingebettete Objekte enthält. Die von der Abfrage zurückgegebenen Ergebnisse variieren abhängig von der Form der Abfrage, die Sie verwenden.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Abfragen von eingebetteten Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed2e13bd9d9dc798891a723a6fed1b1734e1735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755056"
---
# <a name="querying-embedded-objects"></a><span data-ttu-id="8de8c-104">Abfragen von eingebetteten Objekten</span><span class="sxs-lookup"><span data-stu-id="8de8c-104">Querying Embedded Objects</span></span>

<span data-ttu-id="8de8c-105">Es gibt mehrere Möglichkeiten, wie eine Abfrage eine Abfrage durchführt, wenn eine Ereignisklasse abgefragt wird, die eingebettete Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="8de8c-105">You have several options as to the form a query takes when querying an event class that contains embedded objects.</span></span> <span data-ttu-id="8de8c-106">Die von der Abfrage zurückgegebenen Ergebnisse variieren abhängig von der Form der Abfrage, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="8de8c-106">The results returned by the query vary, depending on the form of the query you use.</span></span>

## <a name="class-definitions"></a><span data-ttu-id="8de8c-107">Klassendefinitionen</span><span class="sxs-lookup"><span data-stu-id="8de8c-107">Class Definitions</span></span>

<span data-ttu-id="8de8c-108">Das folgende Beispiel zeigt die Klassendefinitionen, die für die WQL-Abfragen in diesem Thema verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8de8c-108">The following example shows the class definitions that are used for the WQL queries in this topic.</span></span>

``` syntax
class MyClass
{
   string Prop1;
   string Prop2;
};

class MyEvent : __ExtrinsicEvent
{
   MyClass E1;
   MyClass E2;
};
```

## <a name="examples"></a><span data-ttu-id="8de8c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8de8c-109">Examples</span></span>

<span data-ttu-id="8de8c-110">Die folgende Abfrage gibt sowohl die eingebetteten Klassen **E1** als auch **E2** zurück, die jeweils **Eigenschaft PROP1** und **Prop2** mit Daten aufgefüllt haben.</span><span class="sxs-lookup"><span data-stu-id="8de8c-110">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`SELECT * FROM MyEvent`

<span data-ttu-id="8de8c-111">Die folgende Abfrage gibt das **E1** Embedded-Objekt zurück, wobei jedoch weder **Eigenschaft PROP1** noch **Prop2** mit Daten aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="8de8c-111">The following query returns the **E1** embedded object, but with neither **Prop1** nor **Prop2** populated with data.</span></span>

`SELECT E1 FROM MyEvent`

<span data-ttu-id="8de8c-112">Die folgende Abfrage gibt die eingebettete Klasse **E1** zurück, wobei nur **Eigenschaft PROP1** mit Daten aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="8de8c-112">The following query returns the embedded class **E1** with only **Prop1** populated with data.</span></span>

`SELECT E1.Prop1 FROM MyEvent`

<span data-ttu-id="8de8c-113">Die folgende Abfrage gibt sowohl die eingebetteten Klassen **E1** als auch **E2** zurück, die jeweils **Eigenschaft PROP1** und **Prop2** mit Daten aufgefüllt haben.</span><span class="sxs-lookup"><span data-stu-id="8de8c-113">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

<span data-ttu-id="8de8c-114">Dies entspricht der ersten Abfrage mit dem Sternchen ( \* ) anstelle der Angabe der einzelnen Objekte und Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8de8c-114">This is equivalent to the first query using the asterisk (\*) instead of specifying each object and property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8de8c-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8de8c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8de8c-116">Abfragen mit WQL</span><span class="sxs-lookup"><span data-stu-id="8de8c-116">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

 



