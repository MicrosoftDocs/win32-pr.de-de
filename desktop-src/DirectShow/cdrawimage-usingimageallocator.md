---
description: Die usingimagezuordcator-Methode gibt an, ob die aktuelle Zuweisung ein cimagezuordcator-Objekt ist.
ms.assetid: 842bbcbc-2cc8-4e9d-b6c0-e07f7e472ca1
title: Cdrawimage. usingimagezuordcator-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UsingImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a61b4ece94c9c52a0f769a29ec32a26c08b33ee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370859"
---
# <a name="cdrawimageusingimageallocator-method"></a><span data-ttu-id="11ab7-103">Cdrawimage. usingimagezuordcator-Methode</span><span class="sxs-lookup"><span data-stu-id="11ab7-103">CDrawImage.UsingImageAllocator method</span></span>

<span data-ttu-id="11ab7-104">Die- `UsingImageAllocator` Methode gibt an, ob die aktuelle Zuweisung ein [**cimagezuordcator**](cimageallocator.md) -Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="11ab7-104">The `UsingImageAllocator` method indicates whether the current allocator is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="11ab7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11ab7-105">Syntax</span></span>


```C++
BOOL UsingImageAllocator();
```



## <a name="parameters"></a><span data-ttu-id="11ab7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11ab7-106">Parameters</span></span>

<span data-ttu-id="11ab7-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="11ab7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11ab7-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11ab7-108">Return value</span></span>

<span data-ttu-id="11ab7-109">Gibt **true** zurück, wenn die aktuelle Zuweisung ein **cimagezuordnerobjekt** ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="11ab7-109">Returns **TRUE** if the current allocator is a **CImageAllocator** object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="11ab7-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11ab7-110">Requirements</span></span>



| <span data-ttu-id="11ab7-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11ab7-111">Requirement</span></span> | <span data-ttu-id="11ab7-112">Wert</span><span class="sxs-lookup"><span data-stu-id="11ab7-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11ab7-113">Header</span><span class="sxs-lookup"><span data-stu-id="11ab7-113">Header</span></span><br/>  | <dl> <span data-ttu-id="11ab7-114"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11ab7-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="11ab7-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11ab7-115">Library</span></span><br/> | <dl> <span data-ttu-id="11ab7-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="11ab7-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11ab7-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11ab7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ab7-118">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="11ab7-118">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="11ab7-119">**Cdrawimage:: notifyzucator**</span><span class="sxs-lookup"><span data-stu-id="11ab7-119">**CDrawImage::NotifyAllocator**</span></span>](cdrawimage-notifyallocator.md)
</dt> </dl>

 

 




