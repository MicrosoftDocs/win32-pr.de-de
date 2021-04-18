---
description: Die notifyzucator-Methode informiert das cdrawimage-Objekt darüber, ob die Zuweisung für die Verbindung ein cimagezuordcator-Objekt ist.
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: Cdrawimage. notifyzucator-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7bab7d1d00b70317a7cbb0b79f8a430a603a757
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352083"
---
# <a name="cdrawimagenotifyallocator-method"></a><span data-ttu-id="59b8b-103">Cdrawimage. notifyzucator-Methode</span><span class="sxs-lookup"><span data-stu-id="59b8b-103">CDrawImage.NotifyAllocator method</span></span>

<span data-ttu-id="59b8b-104">Die- `NotifyAllocator` Methode informiert das **cdrawimage** -Objekt darüber, ob die Zuweisung für die Verbindung ein [**cimagezuordcator**](cimageallocator.md) -Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="59b8b-104">The `NotifyAllocator` method informs the **CDrawImage** object whether the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b8b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59b8b-105">Syntax</span></span>


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="59b8b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59b8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b8b-107">*busingimagezuordcator*</span><span class="sxs-lookup"><span data-stu-id="59b8b-107">*bUsingImageAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="59b8b-108">Boolescher Wert, der angibt, welche Art von Zuweisungstyp verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="59b8b-108">Boolean value that indicates what kind of allocator is being used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b8b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59b8b-109">Return value</span></span>

<span data-ttu-id="59b8b-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="59b8b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59b8b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59b8b-111">Remarks</span></span>

<span data-ttu-id="59b8b-112">Der besitzende Filter sollte diese Methode anrufen, nachdem die Pins einem Zuweiser zugestimmt haben.</span><span class="sxs-lookup"><span data-stu-id="59b8b-112">The owning filter should call this method after the pins agree to an allocator.</span></span> <span data-ttu-id="59b8b-113">Wenn der Filter weiß, dass es sich bei der Zuweisung um ein **cimagezuordnerobjekt** handelt, sollte diese Methode mit dem Wert " **true**" aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="59b8b-113">If the filter knows the allocator is a **CImageAllocator** object, it should call this method with the value **TRUE**.</span></span> <span data-ttu-id="59b8b-114">(In der Regel kennt der Filter dies nur, wenn er die betreffende Zuweisung besitzt.) Andernfalls sollte diese Methode mit dem Wert **false** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="59b8b-114">(Typically, the filter will know this only if it owns the allocator in question.) Otherwise, it should call this method with the value **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b8b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59b8b-115">Requirements</span></span>



| <span data-ttu-id="59b8b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59b8b-116">Requirement</span></span> | <span data-ttu-id="59b8b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="59b8b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59b8b-118">Header</span><span class="sxs-lookup"><span data-stu-id="59b8b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="59b8b-119"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59b8b-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59b8b-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="59b8b-120">Library</span></span><br/> | <dl> <span data-ttu-id="59b8b-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="59b8b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b8b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59b8b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b8b-123">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="59b8b-123">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="59b8b-124">**Cdrawimage::D rawImage**</span><span class="sxs-lookup"><span data-stu-id="59b8b-124">**CDrawImage::DrawImage**</span></span>](cdrawimage-drawimage.md)
</dt> </dl>

 

 




