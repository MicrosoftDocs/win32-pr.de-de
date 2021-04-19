---
description: Die Methode "Zuweisung" weist Speicher für die Puffer zu.
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: Cbasezucator. Zuordnungsmethode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7510a108e69eb218a894b67dd5b62d94bfdbe6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367415"
---
# <a name="cbaseallocatoralloc-method"></a><span data-ttu-id="0bf3f-103">Cbasezucator. Zuordnungsmethode</span><span class="sxs-lookup"><span data-stu-id="0bf3f-103">CBaseAllocator.Alloc method</span></span>

<span data-ttu-id="0bf3f-104">Die- `Alloc` Methode weist Speicher für die Puffer zu.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bf3f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bf3f-105">Syntax</span></span>


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="0bf3f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bf3f-106">Parameters</span></span>

<span data-ttu-id="0bf3f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0bf3f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bf3f-108">Return value</span></span>

<span data-ttu-id="0bf3f-109">Gibt einen der folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="0bf3f-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0bf3f-110">Return code</span></span>                                                                                       | <span data-ttu-id="0bf3f-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bf3f-111">Description</span></span>                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="0bf3f-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0bf3f-112"><dt>**S\_FALSE**</dt></span></span> </dl>           | <span data-ttu-id="0bf3f-113">Die Puffer Anforderungen wurden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-113">Buffer requirements have not changed.</span></span><br/> |
| <dl> <span data-ttu-id="0bf3f-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0bf3f-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="0bf3f-115">Die Puffer Anforderungen wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-115">Buffer requirements have changed.</span></span><br/>     |
| <dl> <span data-ttu-id="0bf3f-116"><dt>**VFW \_ E \_ sizenotset**</dt></span><span class="sxs-lookup"><span data-stu-id="0bf3f-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="0bf3f-117">Die Puffer Anforderungen wurden nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-117">Buffer requirements were not set.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="0bf3f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bf3f-118">Remarks</span></span>

<span data-ttu-id="0bf3f-119">Diese Methode wird von der [**cbasezucator:: Commit**](cbaseallocator-commit.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span>

<span data-ttu-id="0bf3f-120">In der-Basisklasse weist diese Methode keinen Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-120">In the base class, this method does not allocate any memory.</span></span> <span data-ttu-id="0bf3f-121">Es wird ein Fehler zurückgegeben, wenn die Puffer Anforderungen nicht festgelegt wurden, s \_ false, wenn die Anforderungen nicht geändert wurden, und s \_ OK, wenn sich die Anforderungen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-121">It returns an error if the buffer requirements were not set, S\_FALSE if the requirements have not changed, and S\_OK if the requirements have changed.</span></span>

<span data-ttu-id="0bf3f-122">Eine abgeleitete Klasse sollte diese Methode überschreiben, um die tatsächliche Speicher Belegung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-122">A derived class should override this method to perform the actual memory allocation.</span></span> <span data-ttu-id="0bf3f-123">In der Regel führt die abgeleitete Klasse die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0bf3f-123">Typically, the derived class will perform the following steps:</span></span>

1.  <span data-ttu-id="0bf3f-124">Nennen Sie die Basisklassen Implementierung, um zu bestimmen, ob der Arbeitsspeicher wirklich zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-124">Call the base class implementation, to determine whether the memory truly needs allocating.</span></span>
2.  <span data-ttu-id="0bf3f-125">Arbeitsspeicher zuweisen.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-125">Allocate memory.</span></span>
3.  <span data-ttu-id="0bf3f-126">Erstellen Sie [**cmediasample**](cmediasample.md) -Objekte, die Arbeitsspeicher Blöcke aus Schritt 2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="0bf3f-126">Create [**CMediaSample**](cmediasample.md) objects that contain chunks of memory from step 2.</span></span>
4.  <span data-ttu-id="0bf3f-127">Fügen Sie jedes **cmediasample** -Objekt der Liste der kostenlosen Beispiele hinzu ([**cbasezucator:: m \_ lfree**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="0bf3f-127">Add each **CMediaSample** object to the list of free samples ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>

<span data-ttu-id="0bf3f-128">Ein Beispiel finden Sie unter [**cmemzuordcator:: Zuweisung**](cmemallocator-alloc.md).</span><span class="sxs-lookup"><span data-stu-id="0bf3f-128">For an example, see [**CMemAllocator::Alloc**](cmemallocator-alloc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bf3f-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bf3f-129">Requirements</span></span>



| <span data-ttu-id="0bf3f-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bf3f-130">Requirement</span></span> | <span data-ttu-id="0bf3f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="0bf3f-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf3f-132">Header</span><span class="sxs-lookup"><span data-stu-id="0bf3f-132">Header</span></span><br/>  | <dl> <span data-ttu-id="0bf3f-133"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0bf3f-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0bf3f-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0bf3f-134">Library</span></span><br/> | <dl> <span data-ttu-id="0bf3f-135">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0bf3f-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bf3f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bf3f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf3f-137">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0bf3f-137">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




