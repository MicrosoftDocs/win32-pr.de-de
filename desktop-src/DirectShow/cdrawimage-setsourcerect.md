---
description: Die setsourcerect-Methode legt das Quell Rechteck fest.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Cdrawimage. setsourcerect-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370566"
---
# <a name="cdrawimagesetsourcerect-method"></a><span data-ttu-id="1eb60-103">Cdrawimage. setsourcerect-Methode</span><span class="sxs-lookup"><span data-stu-id="1eb60-103">CDrawImage.SetSourceRect method</span></span>

<span data-ttu-id="1eb60-104">Die- `SetSourceRect` Methode legt das Quell Rechteck fest.</span><span class="sxs-lookup"><span data-stu-id="1eb60-104">The `SetSourceRect` method sets the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb60-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1eb60-105">Syntax</span></span>


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="1eb60-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1eb60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eb60-107">*psourcerect*</span><span class="sxs-lookup"><span data-stu-id="1eb60-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="1eb60-108">Zeiger auf eine **Rect** -Struktur, die das neue Quell Rechteck definiert.</span><span class="sxs-lookup"><span data-stu-id="1eb60-108">Pointer to a **RECT** structure that defines the new source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eb60-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1eb60-109">Return value</span></span>

<span data-ttu-id="1eb60-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1eb60-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eb60-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1eb60-111">Remarks</span></span>

<span data-ttu-id="1eb60-112">Der besitzende Filter sollte diese Methode beim Ändern des Quell Rechtecks aufruft. beispielsweise als Reaktion auf einen [**ibasicvideo:: setsourceposition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="1eb60-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) call.</span></span>

<span data-ttu-id="1eb60-113">Überprüfen Sie das in *psourcerect* angegebene Rechteck, bevor Sie diese Methode aufrufen, um sicherzustellen, dass Sie nicht über die systemeigene Videogröße hinaus erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="1eb60-113">Validate the rectangle given in *pSourceRect* before calling this method, to make sure it does not extend beyond the native video size.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb60-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1eb60-114">Requirements</span></span>



| <span data-ttu-id="1eb60-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1eb60-115">Requirement</span></span> | <span data-ttu-id="1eb60-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1eb60-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb60-117">Header</span><span class="sxs-lookup"><span data-stu-id="1eb60-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1eb60-118"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1eb60-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1eb60-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1eb60-119">Library</span></span><br/> | <dl> <span data-ttu-id="1eb60-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1eb60-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eb60-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1eb60-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb60-122">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1eb60-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




