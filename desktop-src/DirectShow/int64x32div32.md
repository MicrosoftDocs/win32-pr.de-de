---
description: Die Int64x32Div32-Funktion implementiert die Formel ((a \* b) + Rnd)/c wobei a ein 64-Bit-Wert ist und b, c und Rnd 32-Bit-Werte sind.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Int64x32Div32-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de60ca08b262dbf97aa118bd115bd6dc58576a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361671"
---
# <a name="int64x32div32-function"></a><span data-ttu-id="1386b-103">Int64x32Div32-Funktion</span><span class="sxs-lookup"><span data-stu-id="1386b-103">Int64x32Div32 function</span></span>

<span data-ttu-id="1386b-104">Die `Int64x32Div32` -Funktion implementiert die Formel, `((a*b)+rnd)/c` bei der *ein* 64-Bit-Wert ist und *b*, *c* und *Rnd* 32-Bit-Werte sind.</span><span class="sxs-lookup"><span data-stu-id="1386b-104">The `Int64x32Div32` function implements the formula `((a*b)+rnd)/c` where *a* is a 64-bit value and *b*, *c*, and *rnd* are 32-bit values.</span></span>

## <a name="syntax"></a><span data-ttu-id="1386b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1386b-105">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
);
```



## <a name="parameters"></a><span data-ttu-id="1386b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1386b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1386b-107">*ein*</span><span class="sxs-lookup"><span data-stu-id="1386b-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="1386b-108">Multiplikand.</span><span class="sxs-lookup"><span data-stu-id="1386b-108">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="1386b-109">*b*</span><span class="sxs-lookup"><span data-stu-id="1386b-109">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="1386b-110">Multiplikator.</span><span class="sxs-lookup"><span data-stu-id="1386b-110">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="1386b-111">*c*</span><span class="sxs-lookup"><span data-stu-id="1386b-111">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="1386b-112">Divisor.</span><span class="sxs-lookup"><span data-stu-id="1386b-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="1386b-113">*Rnd*</span><span class="sxs-lookup"><span data-stu-id="1386b-113">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1386b-114">Rundungs Faktor.</span><span class="sxs-lookup"><span data-stu-id="1386b-114">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1386b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1386b-115">Return value</span></span>

<span data-ttu-id="1386b-116">Gibt entweder die `(a * b + rnd)/c` Berechnung oder einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="1386b-116">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="1386b-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1386b-117">Return code</span></span>                                                                                       | <span data-ttu-id="1386b-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1386b-118">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1386b-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="1386b-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="1386b-120">Ein Überlauf ist aufgetreten, da das Ergebnis zu groß ist (positiv).</span><span class="sxs-lookup"><span data-stu-id="1386b-120">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="1386b-121"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="1386b-121"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="1386b-122">Ein Überlauf ist aufgetreten, da das Ergebnis zu groß (negativ) ist.</span><span class="sxs-lookup"><span data-stu-id="1386b-122">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1386b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1386b-123">Remarks</span></span>

<span data-ttu-id="1386b-124">Rundung für die Division liegt in Richtung NULL.</span><span class="sxs-lookup"><span data-stu-id="1386b-124">Rounding on the division is toward zero.</span></span> <span data-ttu-id="1386b-125">Die Division durch 0 (null) wird als Überlauf Bedingung gezählt.</span><span class="sxs-lookup"><span data-stu-id="1386b-125">Division by zero is counted as an overflow condition.</span></span>

<span data-ttu-id="1386b-126">Zeitstempel und Suchzeiten sind 64-Bit-Werte, sodass diese Funktion zum Ausführen von Konvertierungen auf 32-Bit-Systemen nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="1386b-126">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="1386b-127">In MPEG-1 beträgt die Systemuhr beispielsweise 90-kHz oder 90.000 Ticks pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="1386b-127">For example, in MPEG-1 the system clock reference is 90-kHz, or 90,000 ticks per second.</span></span> <span data-ttu-id="1386b-128">Die Formel zum Konvertieren dieses in eine Verweis Zeit (100-Nanosecond-Einheiten) ist</span><span class="sxs-lookup"><span data-stu-id="1386b-128">The formula to convert this to reference time (100-nanosecond units) is</span></span>


```C++
(timestamp * 1000) / 9
```



<span data-ttu-id="1386b-129">, die als berechnet werden können `Int64x32Div32(timestamp, 1000, 9, 0)` .</span><span class="sxs-lookup"><span data-stu-id="1386b-129">which can be calculated as `Int64x32Div32(timestamp, 1000, 9, 0)`.</span></span> <span data-ttu-id="1386b-130">Verwenden Sie den *Rnd* -Parameter als Rundungs Faktor.</span><span class="sxs-lookup"><span data-stu-id="1386b-130">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="1386b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1386b-131">Requirements</span></span>



| <span data-ttu-id="1386b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1386b-132">Requirement</span></span> | <span data-ttu-id="1386b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1386b-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1386b-134">Header</span><span class="sxs-lookup"><span data-stu-id="1386b-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1386b-135"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1386b-135"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1386b-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1386b-136">Library</span></span><br/> | <dl> <span data-ttu-id="1386b-137">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1386b-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1386b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1386b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1386b-139">Diverse Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="1386b-139">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="1386b-140">**llmuldiv**</span><span class="sxs-lookup"><span data-stu-id="1386b-140">**llMulDiv**</span></span>](llmuldiv.md)
</dt> </dl>

 

 




