---
description: Konstruktormethode.
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Cmediasample. cmediasample-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4513af3b01d39f311fd1b8ecc1cea8f086d89c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358322"
---
# <a name="cmediasamplecmediasample-constructor"></a><span data-ttu-id="feb8f-103">Cmediasample. cmediasample-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="feb8f-103">CMediaSample.CMediaSample constructor</span></span>

<span data-ttu-id="feb8f-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="feb8f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb8f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="feb8f-105">Syntax</span></span>


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a><span data-ttu-id="feb8f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="feb8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feb8f-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="feb8f-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="feb8f-108">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="feb8f-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="feb8f-109">*pallocator*</span><span class="sxs-lookup"><span data-stu-id="feb8f-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="feb8f-110">Zeiger auf das [**cbasezucator**](cbaseallocator.md) -Objekt, das das Beispiel erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="feb8f-110">Pointer to the [**CBaseAllocator**](cbaseallocator.md) object that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="feb8f-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="feb8f-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="feb8f-112">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="feb8f-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="feb8f-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="feb8f-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="feb8f-114">Zeiger auf einen vom Aufrufer zugeordneten Speicherpuffer mit einer Größen *Länge*.</span><span class="sxs-lookup"><span data-stu-id="feb8f-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span>

</dd> <dt>

<span data-ttu-id="feb8f-115">*length*</span><span class="sxs-lookup"><span data-stu-id="feb8f-115">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="feb8f-116">Länge des Speicherpuffers.</span><span class="sxs-lookup"><span data-stu-id="feb8f-116">Length of the memory buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="feb8f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="feb8f-117">Remarks</span></span>

<span data-ttu-id="feb8f-118">Der **HRESULT** -Wert, der im *PHR* -Parameter übergeben wird, wird von der Basisklasse nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="feb8f-118">The base class does not modify the **HRESULT** value passed in the *phr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb8f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="feb8f-119">Requirements</span></span>



| <span data-ttu-id="feb8f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="feb8f-120">Requirement</span></span> | <span data-ttu-id="feb8f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="feb8f-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb8f-122">Header</span><span class="sxs-lookup"><span data-stu-id="feb8f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="feb8f-123"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="feb8f-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="feb8f-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="feb8f-124">Library</span></span><br/> | <dl> <span data-ttu-id="feb8f-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="feb8f-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feb8f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="feb8f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb8f-127">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="feb8f-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




