---
description: Die Methode "count prefixbits" berechnet die Anzahl der Bits (0) am Anfang eines angegebenen Bitfelds.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Cimagedisplay. countrytprefixbits-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4333e1b0826b4fac7bfff463531b5d2e10704418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371423"
---
# <a name="cimagedisplaycountprefixbits-method"></a><span data-ttu-id="fd495-103">Cimagedisplay. countrytprefixbits-Methode</span><span class="sxs-lookup"><span data-stu-id="fd495-103">CImageDisplay.CountPrefixBits method</span></span>

<span data-ttu-id="fd495-104">Die- `CountPrefixBits` Methode berechnet die Anzahl der Bits (0) am Anfang eines angegebenen Bitfelds.</span><span class="sxs-lookup"><span data-stu-id="fd495-104">The `CountPrefixBits` method calculates the number of zero bits at the start of a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd495-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd495-105">Syntax</span></span>


```C++
DWORD CountPrefixBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="fd495-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd495-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd495-107">*Feld*</span><span class="sxs-lookup"><span data-stu-id="fd495-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="fd495-108">Gibt ein Bitfeld als **DWORD** -Wert an.</span><span class="sxs-lookup"><span data-stu-id="fd495-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd495-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd495-109">Return value</span></span>

<span data-ttu-id="fd495-110">Gibt die Anzahl von Null Bits zurück, die vor dem ersten 1 Bit auftreten, oder 0x80000000, wenn alle Bits 0 (null) sind.</span><span class="sxs-lookup"><span data-stu-id="fd495-110">Returns the number of zero bits that occur before the first 1 bit, or 0x80000000 if all bits are zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd495-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd495-111">Remarks</span></span>

<span data-ttu-id="fd495-112">Diese Methode eignet sich für die Arbeit mit Farb Masken in [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="fd495-112">This method is useful for working with color masks in [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd495-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd495-113">Requirements</span></span>



| <span data-ttu-id="fd495-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd495-114">Requirement</span></span> | <span data-ttu-id="fd495-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fd495-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd495-116">Header</span><span class="sxs-lookup"><span data-stu-id="fd495-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fd495-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd495-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fd495-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fd495-118">Library</span></span><br/> | <dl> <span data-ttu-id="fd495-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fd495-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd495-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd495-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd495-121">**Cimagedisplay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fd495-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




