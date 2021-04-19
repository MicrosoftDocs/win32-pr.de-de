---
description: Ruft das nächste Element aus der Warteschlange ab.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Cqueue. getqueueobject-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356025"
---
# <a name="cqueuegetqueueobject-method"></a><span data-ttu-id="7351f-103">Cqueue. getqueueobject-Methode</span><span class="sxs-lookup"><span data-stu-id="7351f-103">CQueue.GetQueueObject method</span></span>

<span data-ttu-id="7351f-104">Ruft das nächste Element aus der Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="7351f-104">Retrieves the next item from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="7351f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7351f-105">Syntax</span></span>


```C++
T GetQueueObject();
```



## <a name="parameters"></a><span data-ttu-id="7351f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7351f-106">Parameters</span></span>

<span data-ttu-id="7351f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7351f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7351f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7351f-108">Return value</span></span>

<span data-ttu-id="7351f-109">Gibt ein Objekt vom Typ **T** zurück (den Vorlagentyp).</span><span class="sxs-lookup"><span data-stu-id="7351f-109">Returns an object of type **T** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="7351f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7351f-110">Remarks</span></span>

<span data-ttu-id="7351f-111">Diese Methode wird blockiert, bis ein Element in der Warteschlange verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7351f-111">This method blocks until an item is available on the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="7351f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7351f-112">Requirements</span></span>



| <span data-ttu-id="7351f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7351f-113">Requirement</span></span> | <span data-ttu-id="7351f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7351f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7351f-115">Header</span><span class="sxs-lookup"><span data-stu-id="7351f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7351f-116"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7351f-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7351f-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7351f-117">Library</span></span><br/> | <dl> <span data-ttu-id="7351f-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7351f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7351f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7351f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7351f-120">**Cqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7351f-120">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




