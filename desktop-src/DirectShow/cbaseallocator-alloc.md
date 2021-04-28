---
description: 'CBaseAllocator.Alloc-Methode: Die Alloc-Methode weist den Puffern Arbeitsspeicher zu.'
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: CBaseAllocator.Alloc-Methode (Amfilter.h)
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
ms.openlocfilehash: b53dc461a520b4e8c890a36fca6d73c2c836499f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096367"
---
# <a name="cbaseallocatoralloc-method"></a><span data-ttu-id="037f1-103">CBaseAllocator.Alloc-Methode</span><span class="sxs-lookup"><span data-stu-id="037f1-103">CBaseAllocator.Alloc method</span></span>

<span data-ttu-id="037f1-104">Die `Alloc` -Methode weist Den Puffern Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="037f1-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="037f1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="037f1-105">Syntax</span></span>


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="037f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="037f1-106">Parameters</span></span>

<span data-ttu-id="037f1-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="037f1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="037f1-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="037f1-108">Return value</span></span>

<span data-ttu-id="037f1-109">Gibt einen der folgenden **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="037f1-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="037f1-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="037f1-110">Return code</span></span>                                                                                       | <span data-ttu-id="037f1-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="037f1-111">Description</span></span>                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="037f1-112"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="037f1-112"><dt>**S\_FALSE**</dt></span></span> </dl>           | <span data-ttu-id="037f1-113">Die Pufferanforderungen wurden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="037f1-113">Buffer requirements have not changed.</span></span><br/> |
| <dl> <span data-ttu-id="037f1-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="037f1-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="037f1-115">Die Pufferanforderungen haben sich geändert.</span><span class="sxs-lookup"><span data-stu-id="037f1-115">Buffer requirements have changed.</span></span><br/>     |
| <dl> <span data-ttu-id="037f1-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="037f1-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="037f1-117">Pufferanforderungen wurden nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="037f1-117">Buffer requirements were not set.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="037f1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="037f1-118">Remarks</span></span>

<span data-ttu-id="037f1-119">Diese Methode wird von der [**CBaseAllocator::Commit-Methode**](cbaseallocator-commit.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="037f1-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span>

<span data-ttu-id="037f1-120">In der Basisklasse weist diese Methode keinen Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="037f1-120">In the base class, this method does not allocate any memory.</span></span> <span data-ttu-id="037f1-121">Es wird ein Fehler zurückgegeben, wenn die Pufferanforderungen nicht festgelegt wurden, S FALSE, wenn sich die Anforderungen nicht geändert haben, und S OK, wenn sich \_ \_ die Anforderungen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="037f1-121">It returns an error if the buffer requirements were not set, S\_FALSE if the requirements have not changed, and S\_OK if the requirements have changed.</span></span>

<span data-ttu-id="037f1-122">Eine abgeleitete Klasse sollte diese Methode überschreiben, um die tatsächliche Speicherzuweisung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="037f1-122">A derived class should override this method to perform the actual memory allocation.</span></span> <span data-ttu-id="037f1-123">In der Regel führt die abgeleitete Klasse die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="037f1-123">Typically, the derived class will perform the following steps:</span></span>

1.  <span data-ttu-id="037f1-124">Rufen Sie die Basisklassenimplementierung auf, um zu bestimmen, ob für den Arbeitsspeicher tatsächlich eine Zuweisung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="037f1-124">Call the base class implementation, to determine whether the memory truly needs allocating.</span></span>
2.  <span data-ttu-id="037f1-125">Zuordnen von Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="037f1-125">Allocate memory.</span></span>
3.  <span data-ttu-id="037f1-126">Erstellen [**Sie CMediaSample-Objekte,**](cmediasample.md) die Speicherelemente aus Schritt 2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="037f1-126">Create [**CMediaSample**](cmediasample.md) objects that contain chunks of memory from step 2.</span></span>
4.  <span data-ttu-id="037f1-127">Fügen Sie **jedes CMediaSample-Objekt** zur Liste der kostenlosen Beispiele hinzu ([**CBaseAllocator::m \_ lFree**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="037f1-127">Add each **CMediaSample** object to the list of free samples ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>

<span data-ttu-id="037f1-128">Ein Beispiel finden Sie unter [**CMemAllocator::Alloc**](cmemallocator-alloc.md).</span><span class="sxs-lookup"><span data-stu-id="037f1-128">For an example, see [**CMemAllocator::Alloc**](cmemallocator-alloc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="037f1-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="037f1-129">Requirements</span></span>



| <span data-ttu-id="037f1-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="037f1-130">Requirement</span></span> | <span data-ttu-id="037f1-131">Wert</span><span class="sxs-lookup"><span data-stu-id="037f1-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="037f1-132">Header</span><span class="sxs-lookup"><span data-stu-id="037f1-132">Header</span></span><br/>  | <dl> <span data-ttu-id="037f1-133"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="037f1-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="037f1-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="037f1-134">Library</span></span><br/> | <dl> <span data-ttu-id="037f1-135"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="037f1-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="037f1-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="037f1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="037f1-137">**CBaseAllocator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="037f1-137">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




