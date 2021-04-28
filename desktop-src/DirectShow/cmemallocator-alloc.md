---
description: 'CMemAllocator.Alloc-Methode: Die Alloc-Methode belegt Speicher für die Puffer.'
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: CMemAllocator.Alloc-Methode (Amfilter.h)
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
ms.openlocfilehash: 7d7de755aa3b8007a122e43529d16f5e39ca0cb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099038"
---
# <a name="cmemallocatoralloc-method"></a><span data-ttu-id="5c583-103">CMemAllocator.Alloc-Methode</span><span class="sxs-lookup"><span data-stu-id="5c583-103">CMemAllocator.Alloc method</span></span>

<span data-ttu-id="5c583-104">Die `Alloc` -Methode belegt Speicher für die Puffer.</span><span class="sxs-lookup"><span data-stu-id="5c583-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c583-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c583-105">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="5c583-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c583-106">Parameters</span></span>

<span data-ttu-id="5c583-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5c583-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c583-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c583-108">Return value</span></span>

<span data-ttu-id="5c583-109">Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="5c583-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="5c583-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5c583-110">Return code</span></span>                                                                                       | <span data-ttu-id="5c583-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c583-111">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="5c583-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5c583-112"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="5c583-113">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="5c583-113">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="5c583-114"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5c583-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="5c583-115">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5c583-115">Insufficient memory.</span></span><br/>              |
| <dl> <span data-ttu-id="5c583-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="5c583-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="5c583-117">Pufferanforderungen wurden nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5c583-117">Buffer requirements were not set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c583-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c583-118">Remarks</span></span>

<span data-ttu-id="5c583-119">Diese Methode wird von der [**CBaseAllocator::Commit-Methode**](cbaseallocator-commit.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5c583-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span> <span data-ttu-id="5c583-120">Es ordnet einen zusammenhängenden Speicherblock zu, der für die Pufferanforderungen ausreicht, die in der [**CMemAllocator::SetProperties-Methode**](cmemallocator-setproperties.md) angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="5c583-120">It allocates a contiguous block of memory sufficient for the buffer requirements given in the [**CMemAllocator::SetProperties**](cmemallocator-setproperties.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c583-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c583-121">Requirements</span></span>



| <span data-ttu-id="5c583-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c583-122">Requirement</span></span> | <span data-ttu-id="5c583-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5c583-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c583-124">Header</span><span class="sxs-lookup"><span data-stu-id="5c583-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5c583-125"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5c583-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5c583-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5c583-126">Library</span></span><br/> | <dl> <span data-ttu-id="5c583-127"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5c583-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c583-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5c583-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c583-129">**CMemAllocator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5c583-129">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




