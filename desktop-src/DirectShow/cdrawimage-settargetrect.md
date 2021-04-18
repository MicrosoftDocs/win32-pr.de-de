---
description: Die settargetrect-Methode legt das Ziel Rechteck fest.
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: Cdrawimage. settargetrect-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364916"
---
# <a name="cdrawimagesettargetrect-method"></a><span data-ttu-id="94aa8-103">Cdrawimage. settargetrect-Methode</span><span class="sxs-lookup"><span data-stu-id="94aa8-103">CDrawImage.SetTargetRect method</span></span>

<span data-ttu-id="94aa8-104">Die- `SetTargetRect` Methode legt das Ziel Rechteck fest.</span><span class="sxs-lookup"><span data-stu-id="94aa8-104">The `SetTargetRect` method sets the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="94aa8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="94aa8-105">Syntax</span></span>


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="94aa8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="94aa8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94aa8-107">*ptargetrect*</span><span class="sxs-lookup"><span data-stu-id="94aa8-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="94aa8-108">Ein Zeiger auf eine **Rect** -Struktur, die das neue Ziel Rechteck definiert.</span><span class="sxs-lookup"><span data-stu-id="94aa8-108">Pointer to a **RECT** structure that defines the new target rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94aa8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94aa8-109">Return value</span></span>

<span data-ttu-id="94aa8-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="94aa8-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94aa8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94aa8-111">Remarks</span></span>

<span data-ttu-id="94aa8-112">Der besitzende Filter sollte diese Methode beim Ändern des Quell Rechtecks aufruft. beispielsweise als Reaktion auf einen [**ibasicvideo:: setdestinationposition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) -Aufruf.</span><span class="sxs-lookup"><span data-stu-id="94aa8-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) call.</span></span>

<span data-ttu-id="94aa8-113">Überprüfen Sie vor dem Aufrufen dieser Methode das in *ptargetrect* angegebene Rechteck relativ zum Videofenster.</span><span class="sxs-lookup"><span data-stu-id="94aa8-113">Before calling this method, validate the rectangle given in *pTargetRect*, relative to the video window.</span></span>

## <a name="requirements"></a><span data-ttu-id="94aa8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94aa8-114">Requirements</span></span>



| <span data-ttu-id="94aa8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94aa8-115">Requirement</span></span> | <span data-ttu-id="94aa8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="94aa8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94aa8-117">Header</span><span class="sxs-lookup"><span data-stu-id="94aa8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="94aa8-118"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94aa8-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="94aa8-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="94aa8-119">Library</span></span><br/> | <dl> <span data-ttu-id="94aa8-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="94aa8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94aa8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94aa8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94aa8-122">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="94aa8-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




