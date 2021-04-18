---
description: Die Methode "Zuweisung" weist Speicher für die Puffer zu.
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Cmemzuzucator. Zuordnungsmethode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a142f6c0cea6cdb9b18507becabb909ce67b0fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358063"
---
# <a name="cmemallocatoralloc-method"></a><span data-ttu-id="f9461-103">Cmemzuzucator. Zuordnungsmethode</span><span class="sxs-lookup"><span data-stu-id="f9461-103">CMemAllocator.Alloc method</span></span>

<span data-ttu-id="f9461-104">Die- `Alloc` Methode weist Speicher für die Puffer zu.</span><span class="sxs-lookup"><span data-stu-id="f9461-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9461-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9461-105">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="f9461-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9461-106">Parameters</span></span>

<span data-ttu-id="f9461-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f9461-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9461-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9461-108">Return value</span></span>

<span data-ttu-id="f9461-109">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f9461-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="f9461-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f9461-110">Return code</span></span>                                                                                       | <span data-ttu-id="f9461-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9461-111">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f9461-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9461-112"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="f9461-113">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="f9461-113">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="f9461-114"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f9461-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="f9461-115">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f9461-115">Insufficient memory.</span></span><br/>              |
| <dl> <span data-ttu-id="f9461-116"><dt>**VFW \_ E \_ sizenotset**</dt></span><span class="sxs-lookup"><span data-stu-id="f9461-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="f9461-117">Die Puffer Anforderungen wurden nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9461-117">Buffer requirements were not set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9461-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9461-118">Remarks</span></span>

<span data-ttu-id="f9461-119">Diese Methode wird von der [**cbasezucator:: Commit**](cbaseallocator-commit.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f9461-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span> <span data-ttu-id="f9461-120">Er ordnet einen zusammenhängenden Speicherblock zu, der für die in der [**cmembelegcator:: SetProperties**](cmemallocator-setproperties.md) -Methode angegebenen Puffer Anforderungen ausreicht.</span><span class="sxs-lookup"><span data-stu-id="f9461-120">It allocates a contiguous block of memory sufficient for the buffer requirements given in the [**CMemAllocator::SetProperties**](cmemallocator-setproperties.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9461-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9461-121">Requirements</span></span>



| <span data-ttu-id="f9461-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9461-122">Requirement</span></span> | <span data-ttu-id="f9461-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f9461-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9461-124">Header</span><span class="sxs-lookup"><span data-stu-id="f9461-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f9461-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9461-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f9461-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9461-126">Library</span></span><br/> | <dl> <span data-ttu-id="f9461-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f9461-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9461-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9461-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9461-129">**Cmemzuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f9461-129">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




