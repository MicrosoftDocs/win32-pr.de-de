---
description: Die coaref-Zeit Klasse konvertiert Verweis Zeiten zwischen Sekunden und 100-Nanosekunden-Einheiten.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: Coaref Time-Klasse (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851495d69a1e34bd1723c20f88dc4bb86b7a8025
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367527"
---
# <a name="coareftime-class"></a><span data-ttu-id="c9e91-103">Coaref Time-Klasse</span><span class="sxs-lookup"><span data-stu-id="c9e91-103">COARefTime class</span></span>

![coaref Time-Klassenhierarchie](images/cutil05.png)

<span data-ttu-id="c9e91-105">Die `COARefTime` -Klasse konvertiert Verweis Zeiten zwischen Sekunden und 100-Nanosekunden-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="c9e91-105">The `COARefTime` class converts reference times between seconds and 100-nanosecond units.</span></span>

<span data-ttu-id="c9e91-106">Diese Klasse konvertiert zwischen Verweis Zeiten, die mit Automatisierungs-und Bezugszeiten kompatibel sind, die mit C/C++ kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="c9e91-106">This class converts between reference times that are compatible with Automation and reference times that are compatible with C/C++.</span></span> <span data-ttu-id="c9e91-107">Automation-kompatible Schnittstellen verwenden **doppelte** Werte, um die Zeit in Sekunden darzustellen.</span><span class="sxs-lookup"><span data-stu-id="c9e91-107">Automation-compatible interfaces use **double** values to represent time in seconds.</span></span> <span data-ttu-id="c9e91-108">Andere Schnittstellen verwenden 64-Bit- **Longlong** -Werte, um die Zeit in 100-Nanosecond-Einheiten darzustellen.</span><span class="sxs-lookup"><span data-stu-id="c9e91-108">Other interfaces use 64-bit **LONGLONG** values to represent time in 100-nanosecond units.</span></span> <span data-ttu-id="c9e91-109">Die folgenden Typen werden für diese Werte definiert:</span><span class="sxs-lookup"><span data-stu-id="c9e91-109">The following types are defined for these values:</span></span>

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

<span data-ttu-id="c9e91-110">Filter können die- `COARefTime` Klasse verwenden, um zwischen den beiden Formaten zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c9e91-110">Filters can use the `COARefTime` class to convert between the two formats.</span></span> <span data-ttu-id="c9e91-111">Diese Klasse wird [**von der Klasse "Klasse"**](creftime.md) abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c9e91-111">This class is derived from the [**CRefTime**](creftime.md) class.</span></span>



| <span data-ttu-id="c9e91-112">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="c9e91-112">Public Methods</span></span>                                          | <span data-ttu-id="c9e91-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9e91-113">Description</span></span>                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="c9e91-114">**Coaref-Zeit**</span><span class="sxs-lookup"><span data-stu-id="c9e91-114">**COARefTime**</span></span>](coareftime-coareftime.md)             | <span data-ttu-id="c9e91-115">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="c9e91-115">Constructor method.</span></span>                                                   |
| <span data-ttu-id="c9e91-116">Operatoren</span><span class="sxs-lookup"><span data-stu-id="c9e91-116">Operators</span></span>                                               | <span data-ttu-id="c9e91-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9e91-117">Description</span></span>                                                           |
| [<span data-ttu-id="c9e91-118">**double**</span><span class="sxs-lookup"><span data-stu-id="c9e91-118">**double**</span></span>](coareftime-double.md)                     | <span data-ttu-id="c9e91-119">Konvertiert die Verweis Zeit in einen **Double** -Wert.</span><span class="sxs-lookup"><span data-stu-id="c9e91-119">Converts the reference time to a **double** value.</span></span>                    |
| [<span data-ttu-id="c9e91-120">**Verweis \_ Zeit**</span><span class="sxs-lookup"><span data-stu-id="c9e91-120">**REFERENCE\_TIME**</span></span>](coareftime-reference-time.md)    | <span data-ttu-id="c9e91-121">Wandelt das Objekt in einen **Verweis \_ Zeitwert** um.</span><span class="sxs-lookup"><span data-stu-id="c9e91-121">Casts the object to a **REFERENCE\_TIME** value.</span></span>                      |
| [<span data-ttu-id="c9e91-122">**Operator =**</span><span class="sxs-lookup"><span data-stu-id="c9e91-122">**operator =**</span></span>](coareftime-operator-assign.md)        | <span data-ttu-id="c9e91-123">Weist eine neue Verweis Zeit zu.</span><span class="sxs-lookup"><span data-stu-id="c9e91-123">Assigns a new reference time.</span></span>                                         |
| [<span data-ttu-id="c9e91-124">**Operator = =**</span><span class="sxs-lookup"><span data-stu-id="c9e91-124">**operator ==**</span></span>](coareftime-operator-eq.md)           | <span data-ttu-id="c9e91-125">Testet auf Gleichheit zwischen zwei Verweis Zeiten.</span><span class="sxs-lookup"><span data-stu-id="c9e91-125">Tests for equality between two reference times.</span></span>                       |
| [<span data-ttu-id="c9e91-126">**Operator! =**</span><span class="sxs-lookup"><span data-stu-id="c9e91-126">**operator !=**</span></span>](cmediatype-operator-neq.md)          | <span data-ttu-id="c9e91-127">Prüft auf Ungleichheit zwischen zwei Verweis Zeiten.</span><span class="sxs-lookup"><span data-stu-id="c9e91-127">Tests for inequality between two reference times.</span></span>                     |
| [<span data-ttu-id="c9e91-128">**Operator <**</span><span class="sxs-lookup"><span data-stu-id="c9e91-128">**operator <**</span></span>](coareftime-operator-lt.md)         | <span data-ttu-id="c9e91-129">Testet, ob eine Verweis Zeit kleiner als eine andere ist.</span><span class="sxs-lookup"><span data-stu-id="c9e91-129">Tests if one reference time is less than another.</span></span>                     |
| [<span data-ttu-id="c9e91-130">**Operator >**</span><span class="sxs-lookup"><span data-stu-id="c9e91-130">**operator >**</span></span>](coareftime-operator-gt.md)         | <span data-ttu-id="c9e91-131">Testet, ob eine Verweis Zeit größer als eine andere ist.</span><span class="sxs-lookup"><span data-stu-id="c9e91-131">Tests if one reference time is greater than another.</span></span>                  |
| [<span data-ttu-id="c9e91-132">**Operator <=**</span><span class="sxs-lookup"><span data-stu-id="c9e91-132">**operator <=**</span></span>](coareftime-operator-lteq.md)      | <span data-ttu-id="c9e91-133">Testet, ob eine Verweis Zeit kleiner als oder gleich einem anderen ist.</span><span class="sxs-lookup"><span data-stu-id="c9e91-133">Tests if one reference time is less than or equal to another.</span></span>         |
| [<span data-ttu-id="c9e91-134">**Operator >=**</span><span class="sxs-lookup"><span data-stu-id="c9e91-134">**operator >=**</span></span>](coareftime-operator-gteq.md)      | <span data-ttu-id="c9e91-135">Testet, ob eine Verweis Zeit größer oder gleich einer anderen ist.</span><span class="sxs-lookup"><span data-stu-id="c9e91-135">Tests if one reference time is greater than or equal to another.</span></span>      |
| [<span data-ttu-id="c9e91-136">**Operator +**</span><span class="sxs-lookup"><span data-stu-id="c9e91-136">**operator +**</span></span>](coareftime-operator-plus.md)          | <span data-ttu-id="c9e91-137">Addiert zwei Verweis Zeiten.</span><span class="sxs-lookup"><span data-stu-id="c9e91-137">Adds two reference times.</span></span>                                             |
| [<span data-ttu-id="c9e91-138">\* \*-Operator \* \*</span><span class="sxs-lookup"><span data-stu-id="c9e91-138">\*\*operator  \*\*</span></span>](coareftime-operator-minus.md)         | <span data-ttu-id="c9e91-139">Subtrahiert eine Verweis Zeit von einer anderen.</span><span class="sxs-lookup"><span data-stu-id="c9e91-139">Subtracts one reference time from another.</span></span>                            |
| [<span data-ttu-id="c9e91-140">**Operator + =**</span><span class="sxs-lookup"><span data-stu-id="c9e91-140">**operator +=**</span></span>](coareftime-operator-plus-assign.md)  | <span data-ttu-id="c9e91-141">Addiert zwei Verweis Zeiten und weist das Ergebnis diesem-Objekt zu.</span><span class="sxs-lookup"><span data-stu-id="c9e91-141">Adds two reference times, and assigns the result to this object.</span></span>      |
| [<span data-ttu-id="c9e91-142">**Operator =**</span><span class="sxs-lookup"><span data-stu-id="c9e91-142">**operator  =**</span></span>](coareftime-operator-minus-assign.md) | <span data-ttu-id="c9e91-143">Subtrahiert zwei Verweis Zeiten und weist das Ergebnis diesem-Objekt zu.</span><span class="sxs-lookup"><span data-stu-id="c9e91-143">Subtracts two reference times, and assigns the result to this object.</span></span> |
| [<span data-ttu-id="c9e91-144">**KOM \***</span><span class="sxs-lookup"><span data-stu-id="c9e91-144">**operator \***</span></span>](coareftime-operator-mult.md)         | <span data-ttu-id="c9e91-145">Multipliziert eine Verweis Zeit mit einem Wert.</span><span class="sxs-lookup"><span data-stu-id="c9e91-145">Multiplies a reference time by a value.</span></span>                               |
| [<span data-ttu-id="c9e91-146">**KOM**</span><span class="sxs-lookup"><span data-stu-id="c9e91-146">**operator /**</span></span>](coareftime-operator-div.md)           | <span data-ttu-id="c9e91-147">Dividiert eine Verweis Zeit durch einen-Wert.</span><span class="sxs-lookup"><span data-stu-id="c9e91-147">Divides a reference time by a value.</span></span>                                  |



 

## <a name="requirements"></a><span data-ttu-id="c9e91-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9e91-148">Requirements</span></span>



| <span data-ttu-id="c9e91-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9e91-149">Requirement</span></span> | <span data-ttu-id="c9e91-150">Wert</span><span class="sxs-lookup"><span data-stu-id="c9e91-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9e91-151">Header</span><span class="sxs-lookup"><span data-stu-id="c9e91-151">Header</span></span><br/>  | <dl> <span data-ttu-id="c9e91-152"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9e91-152"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c9e91-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c9e91-153">Library</span></span><br/> | <dl> <span data-ttu-id="c9e91-154">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c9e91-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




