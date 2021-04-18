---
description: Fügt ein Element in die Warteschlange ein.
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: Cqueue. putqueueobject-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.PutQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5371c843bb348f50539535a3df9a0f6aed00893e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361412"
---
# <a name="cqueueputqueueobject-method"></a><span data-ttu-id="b236d-103">Cqueue. putqueueobject-Methode</span><span class="sxs-lookup"><span data-stu-id="b236d-103">CQueue.PutQueueObject method</span></span>

<span data-ttu-id="b236d-104">Fügt ein Element in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="b236d-104">Puts an item onto the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="b236d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b236d-105">Syntax</span></span>


```C++
void PutQueueObject(
   T object
);
```



## <a name="parameters"></a><span data-ttu-id="b236d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b236d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b236d-107">*object*</span><span class="sxs-lookup"><span data-stu-id="b236d-107">*object*</span></span> 
</dt> <dd>

<span data-ttu-id="b236d-108">Ein Objekt vom Typ **T** (der Vorlagentyp).</span><span class="sxs-lookup"><span data-stu-id="b236d-108">Object of type **T** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b236d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b236d-109">Return value</span></span>

<span data-ttu-id="b236d-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b236d-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b236d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b236d-111">Remarks</span></span>

<span data-ttu-id="b236d-112">Diese Methode wird blockiert, bis der Speicherplatz in der Warteschlange für das Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b236d-112">This method blocks until there is space in the queue for the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="b236d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b236d-113">Requirements</span></span>



| <span data-ttu-id="b236d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b236d-114">Requirement</span></span> | <span data-ttu-id="b236d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b236d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b236d-116">Header</span><span class="sxs-lookup"><span data-stu-id="b236d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b236d-117"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b236d-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b236d-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b236d-118">Library</span></span><br/> | <dl> <span data-ttu-id="b236d-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b236d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b236d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b236d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b236d-121">**Cqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b236d-121">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




