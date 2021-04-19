---
description: Die llmuldiv-Funktion implementiert die Formel ((a \* b) + Rnd)/c wobei jeder Begriff ein 64-Bit-Wert ist.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: llmuldiv-Funktion (wxutil. h)
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
ms.openlocfilehash: e45d22eec1536517bd2b57d875dd596e4a1e28db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354141"
---
# <a name="llmuldiv-function"></a><span data-ttu-id="01cf0-103">llmuldiv-Funktion</span><span class="sxs-lookup"><span data-stu-id="01cf0-103">llMulDiv function</span></span>

<span data-ttu-id="01cf0-104">Die `llMulDiv` -Funktion implementiert die Formel, `((a*b)+rnd)/c` bei der jeder Begriff ein 64-Bit-Wert ist.</span><span class="sxs-lookup"><span data-stu-id="01cf0-104">The `llMulDiv` function implements the formula `((a*b)+rnd)/c` where each term is a 64-bit value.</span></span>

<span data-ttu-id="01cf0-105">Zeitstempel und Suchzeiten sind 64-Bit-Werte, sodass diese Funktion zum Ausführen von Konvertierungen auf 32-Bit-Systemen nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="01cf0-105">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="01cf0-106">Die Formel für Bytes pro Sekunde lautet z. b..</span><span class="sxs-lookup"><span data-stu-id="01cf0-106">For example, the formula for bytes-per-second is</span></span>


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



<span data-ttu-id="01cf0-107">, die als berechnet werden können `llMulDiv(nBytes, rtTime, 10000000, 0)` .</span><span class="sxs-lookup"><span data-stu-id="01cf0-107">which can be calculated as `llMulDiv(nBytes, rtTime, 10000000, 0)`.</span></span> <span data-ttu-id="01cf0-108">Verwenden Sie den *Rnd* -Parameter als Rundungs Faktor.</span><span class="sxs-lookup"><span data-stu-id="01cf0-108">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="01cf0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="01cf0-109">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a><span data-ttu-id="01cf0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="01cf0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01cf0-111">*ein*</span><span class="sxs-lookup"><span data-stu-id="01cf0-111">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="01cf0-112">Multiplikand.</span><span class="sxs-lookup"><span data-stu-id="01cf0-112">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="01cf0-113">*b*</span><span class="sxs-lookup"><span data-stu-id="01cf0-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="01cf0-114">Multiplikator.</span><span class="sxs-lookup"><span data-stu-id="01cf0-114">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="01cf0-115">*c*</span><span class="sxs-lookup"><span data-stu-id="01cf0-115">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="01cf0-116">Divisor.</span><span class="sxs-lookup"><span data-stu-id="01cf0-116">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="01cf0-117">*Rnd*</span><span class="sxs-lookup"><span data-stu-id="01cf0-117">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="01cf0-118">Rundungs Faktor.</span><span class="sxs-lookup"><span data-stu-id="01cf0-118">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01cf0-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01cf0-119">Return value</span></span>

<span data-ttu-id="01cf0-120">Gibt entweder die `(a * b + rnd)/c` Berechnung oder einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="01cf0-120">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="01cf0-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="01cf0-121">Return code</span></span>                                                                                       | <span data-ttu-id="01cf0-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01cf0-122">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01cf0-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="01cf0-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="01cf0-124">Ein Überlauf ist aufgetreten, da das Ergebnis zu groß ist (positiv).</span><span class="sxs-lookup"><span data-stu-id="01cf0-124">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="01cf0-125"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="01cf0-125"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="01cf0-126">Ein Überlauf ist aufgetreten, da das Ergebnis zu groß (negativ) ist.</span><span class="sxs-lookup"><span data-stu-id="01cf0-126">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="01cf0-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01cf0-127">Remarks</span></span>

<span data-ttu-id="01cf0-128">Rundung für die Division liegt in Richtung NULL.</span><span class="sxs-lookup"><span data-stu-id="01cf0-128">Rounding on the division is toward zero.</span></span> <span data-ttu-id="01cf0-129">Die Division durch 0 (null) wird als Überlauf Bedingung gezählt.</span><span class="sxs-lookup"><span data-stu-id="01cf0-129">Division by zero is counted as an overflow condition.</span></span>

## <a name="requirements"></a><span data-ttu-id="01cf0-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01cf0-130">Requirements</span></span>



| <span data-ttu-id="01cf0-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01cf0-131">Requirement</span></span> | <span data-ttu-id="01cf0-132">Wert</span><span class="sxs-lookup"><span data-stu-id="01cf0-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01cf0-133">Header</span><span class="sxs-lookup"><span data-stu-id="01cf0-133">Header</span></span><br/>  | <dl> <span data-ttu-id="01cf0-134"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01cf0-134"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="01cf0-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="01cf0-135">Library</span></span><br/> | <dl> <span data-ttu-id="01cf0-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="01cf0-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01cf0-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01cf0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01cf0-138">Diverse Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="01cf0-138">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="01cf0-139">**Int64x32Div32**</span><span class="sxs-lookup"><span data-stu-id="01cf0-139">**Int64x32Div32**</span></span>](int64x32div32.md)
</dt> </dl>

 

 




