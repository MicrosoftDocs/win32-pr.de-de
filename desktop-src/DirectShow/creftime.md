---
description: Die Klasse "kreftime" ist eine Hilfsklasse zum Verwalten von Verweis Zeiten.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: Up-Time-Klasse (Ref time. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01e83520943abafd814425b6ff3fb53f48775627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364957"
---
# <a name="creftime-class"></a><span data-ttu-id="6dd19-103">Klasse "up"</span><span class="sxs-lookup"><span data-stu-id="6dd19-103">CRefTime class</span></span>

![Klassenhierarchie in der Klasse](images/cutil05.png)

<span data-ttu-id="6dd19-105">Die- `CRefTime` Klasse ist eine Hilfsklasse zum Verwalten von Verweis Zeiten.</span><span class="sxs-lookup"><span data-stu-id="6dd19-105">The `CRefTime` class is a helper class for managing reference times.</span></span>

<span data-ttu-id="6dd19-106">Eine *Verweis Zeit* ist eine Zeiteinheit, die in 100-Nanosecond-Einheiten dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6dd19-106">A *reference time* is a unit of time represented in 100-nanosecond units.</span></span> <span data-ttu-id="6dd19-107">Diese Klasse nutzt dasselbe Datenlayout wie der [**Verweis \_ Zeit**](reference-time.md) -Datentyp, fügt jedoch einige Methoden und Operatoren hinzu, die Vergleichs-, Konvertierungs-und arithmetische Funktionen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6dd19-107">This class shares the same data layout as the [**REFERENCE\_TIME**](reference-time.md) data type, but adds some methods and operators that provide comparison, conversion, and arithmetic functions.</span></span> <span data-ttu-id="6dd19-108">Weitere Informationen zu Referenz Zeiten finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="6dd19-108">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>



| <span data-ttu-id="6dd19-109">Öffentliche Element Variablen</span><span class="sxs-lookup"><span data-stu-id="6dd19-109">Public Member Variables</span></span>                                                 | <span data-ttu-id="6dd19-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6dd19-110">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="6dd19-111">**m \_ Zeit**</span><span class="sxs-lookup"><span data-stu-id="6dd19-111">**m\_time**</span></span>](creftime-m-time.md)                                      | <span data-ttu-id="6dd19-112">Gibt den **Verweis \_ Zeitwert** an.</span><span class="sxs-lookup"><span data-stu-id="6dd19-112">Specifies the **REFERENCE\_TIME** value.</span></span>              |
| <span data-ttu-id="6dd19-113">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="6dd19-113">Public Methods</span></span>                                                          | <span data-ttu-id="6dd19-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6dd19-114">Description</span></span>                                           |
| [<span data-ttu-id="6dd19-115">**Zeitpunkt der Aktualisierung**</span><span class="sxs-lookup"><span data-stu-id="6dd19-115">**CRefTime**</span></span>](creftime-creftime.md)                                   | <span data-ttu-id="6dd19-116">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="6dd19-116">Constructor method.</span></span>                                   |
| [<span data-ttu-id="6dd19-117">**Getunits**</span><span class="sxs-lookup"><span data-stu-id="6dd19-117">**GetUnits**</span></span>](creftime-getunits.md)                                   | <span data-ttu-id="6dd19-118">Ruft die Verweis Zeit in 100-Nanosekunden-Einheiten ab.</span><span class="sxs-lookup"><span data-stu-id="6dd19-118">Retrieves the reference time in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="6dd19-119">**Millisekunden**</span><span class="sxs-lookup"><span data-stu-id="6dd19-119">**Millisecs**</span></span>](creftime-millisecs.md)                                 | <span data-ttu-id="6dd19-120">Konvertiert die Verweis Zeit in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="6dd19-120">Converts the reference time to milliseconds.</span></span>          |
| <span data-ttu-id="6dd19-121">Operatoren</span><span class="sxs-lookup"><span data-stu-id="6dd19-121">Operators</span></span>                                                               | <span data-ttu-id="6dd19-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6dd19-122">Description</span></span>                                           |
| [<span data-ttu-id="6dd19-123">**Operator Verweis \_ Zeit ()**</span><span class="sxs-lookup"><span data-stu-id="6dd19-123">**operator REFERENCE\_TIME()**</span></span>](creftime-operator-reference-time-.md) | <span data-ttu-id="6dd19-124">Wandelt das Objekt in einen **Verweis \_ Zeit** Datentyp um.</span><span class="sxs-lookup"><span data-stu-id="6dd19-124">Casts the object to a **REFERENCE\_TIME** data type.</span></span>  |
| [<span data-ttu-id="6dd19-125">**Operator =**</span><span class="sxs-lookup"><span data-stu-id="6dd19-125">**operator=**</span></span>](creftime-operator-assign.md)                           | <span data-ttu-id="6dd19-126">Weist eine neue Verweis Zeit zu.</span><span class="sxs-lookup"><span data-stu-id="6dd19-126">Assigns a new reference time.</span></span>                         |
| [<span data-ttu-id="6dd19-127">**Operator + =**</span><span class="sxs-lookup"><span data-stu-id="6dd19-127">**operator+=**</span></span>](creftime-operator-plus-assign.md)                     | <span data-ttu-id="6dd19-128">Addiert zwei Verweis Zeiten.</span><span class="sxs-lookup"><span data-stu-id="6dd19-128">Adds two reference times.</span></span>                             |
| [<span data-ttu-id="6dd19-129">**Operator =**</span><span class="sxs-lookup"><span data-stu-id="6dd19-129">**operator =**</span></span>](creftime-operator-minus-assign.md)                    | <span data-ttu-id="6dd19-130">Subtrahiert eine Verweis Zeit von einer anderen.</span><span class="sxs-lookup"><span data-stu-id="6dd19-130">Subtracts one reference time from another.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="6dd19-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dd19-131">Remarks</span></span>

<span data-ttu-id="6dd19-132">Bei der Verwendung dieser Klasse ist ein möglicher pitfallwert vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6dd19-132">There is a potential pitfall with using this class.</span></span> <span data-ttu-id="6dd19-133">Wenn Sie den Operator "+ =" mit einem "up"-Objekt als linken Operanden **und einer Variablen** vom Typ " **Long** " als den rechten Operanden anwenden, wandelt der Compiler den rechten Operanden implizit **in ein "** up"-Objekt um.</span><span class="sxs-lookup"><span data-stu-id="6dd19-133">If you apply the += operator with a **CRefTime** object as the left operand and a variable of type **LONG** as the right operand, the compiler will implicitly coerce the right operand into a **CRefTime** object.</span></span> <span data-ttu-id="6dd19-134">Diese Umwandlung **verwendet den "** up"-Konstruktor, der Millisekunden in Bezugs \_ Zeiteinheiten konvertiert. Folglich wird der rechte Operand mit 10.000 multipliziert:</span><span class="sxs-lookup"><span data-stu-id="6dd19-134">This coercion uses the **CRefTime** constructor that converts milliseconds into REFERENCE\_TIME units; as a result, the right operand is multiplied by 10,000:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



<span data-ttu-id="6dd19-135">Dies geschieht jedoch nicht mit dem Operator +:</span><span class="sxs-lookup"><span data-stu-id="6dd19-135">However, the same thing does not happen using the + operator:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a><span data-ttu-id="6dd19-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dd19-136">Requirements</span></span>



| <span data-ttu-id="6dd19-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6dd19-137">Requirement</span></span> | <span data-ttu-id="6dd19-138">Wert</span><span class="sxs-lookup"><span data-stu-id="6dd19-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd19-139">Header</span><span class="sxs-lookup"><span data-stu-id="6dd19-139">Header</span></span><br/>  | <dl> <span data-ttu-id="6dd19-140"><dt>Ref time. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6dd19-140"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6dd19-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6dd19-141">Library</span></span><br/> | <dl> <span data-ttu-id="6dd19-142">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6dd19-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




