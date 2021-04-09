---
description: Die DateAdd-Funktion führt Zeit-und Datumsberechnungen für übereinstimmende Eigenschaften mit Datums Typen aus. Verwenden Sie die Funktion DateAdd, um Datumsangaben und Uhrzeiten in einem angegebenen Zeitraum vor dem aktuellen abzurufen.
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: DATEADD-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128549"
---
# <a name="dateadd-function"></a><span data-ttu-id="c831f-104">DATEADD-Funktion</span><span class="sxs-lookup"><span data-stu-id="c831f-104">DATEADD Function</span></span>

<span data-ttu-id="c831f-105">Die DateAdd-Funktion führt Zeit-und Datumsberechnungen für übereinstimmende Eigenschaften mit Datums Typen aus.</span><span class="sxs-lookup"><span data-stu-id="c831f-105">The DATEADD function performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="c831f-106">Verwenden Sie die Funktion DateAdd, um Datumsangaben und Uhrzeiten in einem angegebenen Zeitraum vor dem aktuellen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c831f-106">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>

## <a name="syntax"></a><span data-ttu-id="c831f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c831f-107">Syntax</span></span>


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a><span data-ttu-id="c831f-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="c831f-108">Arguments</span></span>

<span data-ttu-id="c831f-109">*Datetimeunits*</span><span class="sxs-lookup"><span data-stu-id="c831f-109">*DateTimeUnits*</span></span>

<span data-ttu-id="c831f-110">Gibt die Einheiten des *DateTime* -Parameters an: Jahr, Quartal, Monat, Woche, Tag, Stunde, Minute oder Sekunde.</span><span class="sxs-lookup"><span data-stu-id="c831f-110">Specifies the units of the *DateTime* parameter: YEAR, QUARTER, MONTH, WEEK, DAY, HOUR, MINUTE, or SECOND.</span></span> <span data-ttu-id="c831f-111">Bei diesem Wert wird die Groß-/Kleinschreibung beachtet, und für den Parameter sind keine Anführungszeichen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c831f-111">This value is case-sensitive, and quotation marks are not required around the parameter.</span></span>

<span data-ttu-id="c831f-112">*Offsetvalue*</span><span class="sxs-lookup"><span data-stu-id="c831f-112">*OffsetValue*</span></span>

<span data-ttu-id="c831f-113">Gibt den Zeit Offset in den Einheiten an, die durch den *datetimeunits* -Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c831f-113">Specifies the time offset, in the units specified by the *DateTimeUnits* parameter.</span></span> <span data-ttu-id="c831f-114">**Offsetvalue** muss eine negative Ganzzahl sein.</span><span class="sxs-lookup"><span data-stu-id="c831f-114">**OffsetValue** must be a negative integer.</span></span> <span data-ttu-id="c831f-115">Positive Werte werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c831f-115">Positive values are not supported.</span></span>

<span data-ttu-id="c831f-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="c831f-116">*DateTime*</span></span>

<span data-ttu-id="c831f-117">Gibt einen Zeitstempel an, aus dem der Offset berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c831f-117">Specifies a time stamp from which to calculate the offset.</span></span> <span data-ttu-id="c831f-118">Dies darf kein Datumsliteral sein.</span><span class="sxs-lookup"><span data-stu-id="c831f-118">This cannot be a date literal.</span></span> <span data-ttu-id="c831f-119">Es muss entweder getgmtdate oder das Ergebnis einer anderen DateAdd-Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="c831f-119">It must be either GETGMTDATE or the result of another DATEADD function.</span></span>

## <a name="remarks"></a><span data-ttu-id="c831f-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c831f-120">Remarks</span></span>

<span data-ttu-id="c831f-121">Die DateAdd-Funktion kann nur in literalen Wert vergleichen und nur auf der rechten Seite des Vergleichs Operators verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c831f-121">The DATEADD function can be used only in literal value comparisons and only on the right side of the comparison operator.</span></span>

<span data-ttu-id="c831f-122">Die getgmtdate-Funktion gibt das aktuelle Datum und die aktuelle Uhrzeit in der Ortszeit (Ortszeit) zurück.</span><span class="sxs-lookup"><span data-stu-id="c831f-122">The GETGMTDATE function returns the current date and time in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="c831f-123">Beachten Sie, dass dieser Wert möglicherweise nicht mit der lokalen Zeit des Computers identisch ist.</span><span class="sxs-lookup"><span data-stu-id="c831f-123">Remember that this value may not be the same as the local time of your computer.</span></span>

<span data-ttu-id="c831f-124">Verwenden Sie den Vergleichs Operator "gleich" (=) nicht, da die interne Zeit Darstellung Rundungsfehler verursachen kann, die zu unerwarteten übereinstimmenden Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="c831f-124">Do not use the equals (=) comparison operator because the internal time representation can produce rounding errors that result in unexpected matching results.</span></span>

<span data-ttu-id="c831f-125">Sie können mehrere DateAdd-Funktionen verwenden, um Offset Einheiten zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="c831f-125">You can use multiple DATEADD functions to combine offset units.</span></span>

### <a name="examples"></a><span data-ttu-id="c831f-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c831f-126">Examples</span></span>

<span data-ttu-id="c831f-127">Die folgende Beispiel-WHERE-Klausel stimmt mit Dokumenten überein, die innerhalb der letzten fünf Tage geändert wurden:</span><span class="sxs-lookup"><span data-stu-id="c831f-127">The following example WHERE clause matches documents that were modified within the last five days:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



<span data-ttu-id="c831f-128">Die folgende Beispiel-WHERE-Klausel stimmt mit Dokumenten überein, die innerhalb der letzten zwei Tage und vier Stunden geändert wurden:</span><span class="sxs-lookup"><span data-stu-id="c831f-128">The following example WHERE clause matches documents that were modified within the last two days and four hours:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a><span data-ttu-id="c831f-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c831f-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c831f-130">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="c831f-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c831f-131">Vergleich von literalen Werten</span><span class="sxs-lookup"><span data-stu-id="c831f-131">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="c831f-132">Mehrwertige Vergleiche (Array)</span><span class="sxs-lookup"><span data-stu-id="c831f-132">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="c831f-133">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c831f-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c831f-134">Voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="c831f-134">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="c831f-135">Nicht-voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="c831f-135">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



