---
description: Die Methode "count-setbits" gibt die Anzahl der Bits zurück, die in einem angegebenen Bitfeld auf 1 festgelegt sind.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Cimagedisplay. countrytsetbits-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb425b08b524b1d36b622bcfffcc9f311dccbbdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370913"
---
# <a name="cimagedisplaycountsetbits-method"></a><span data-ttu-id="63809-103">Cimagedisplay. countrytsetbits-Methode</span><span class="sxs-lookup"><span data-stu-id="63809-103">CImageDisplay.CountSetBits method</span></span>

<span data-ttu-id="63809-104">Die- `CountSetBits` Methode gibt die Anzahl von Bits zurück, die in einem angegebenen Bitfeld auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="63809-104">The `CountSetBits` method returns the number of bits set to 1 in a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="63809-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63809-105">Syntax</span></span>


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="63809-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63809-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63809-107">*Feld*</span><span class="sxs-lookup"><span data-stu-id="63809-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="63809-108">Gibt ein Bitfeld als **DWORD** -Wert an.</span><span class="sxs-lookup"><span data-stu-id="63809-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63809-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63809-109">Return value</span></span>

<span data-ttu-id="63809-110">Gibt die Anzahl der Bits zurück, die auf 1 festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="63809-110">Returns the number of bits that are set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="63809-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63809-111">Requirements</span></span>



| <span data-ttu-id="63809-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63809-112">Requirement</span></span> | <span data-ttu-id="63809-113">Wert</span><span class="sxs-lookup"><span data-stu-id="63809-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63809-114">Header</span><span class="sxs-lookup"><span data-stu-id="63809-114">Header</span></span><br/>  | <dl> <span data-ttu-id="63809-115"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63809-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="63809-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="63809-116">Library</span></span><br/> | <dl> <span data-ttu-id="63809-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="63809-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63809-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63809-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63809-119">**Cimagedisplay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="63809-119">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




