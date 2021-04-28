---
description: 'CMediaSample.CMediaSample-Konstruktor : Konstruktormethode.'
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: CMediaSample.CMediaSample-Konstruktor (Amfilter.h)
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
ms.openlocfilehash: 0fd2601b9f53e8f79d9231dd34054932bec4e671
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095438"
---
# <a name="cmediasamplecmediasample-constructor"></a><span data-ttu-id="107e0-103">CMediaSample.CMediaSample-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="107e0-103">CMediaSample.CMediaSample constructor</span></span>

<span data-ttu-id="107e0-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="107e0-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="107e0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="107e0-105">Syntax</span></span>


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a><span data-ttu-id="107e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="107e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="107e0-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="107e0-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="107e0-108">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="107e0-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="107e0-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="107e0-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="107e0-110">Zeiger auf das [**CBaseAllocator-Objekt,**](cbaseallocator.md) das dieses Beispiel erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="107e0-110">Pointer to the [**CBaseAllocator**](cbaseallocator.md) object that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="107e0-111">*Phr*</span><span class="sxs-lookup"><span data-stu-id="107e0-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="107e0-112">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="107e0-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="107e0-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="107e0-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="107e0-114">Zeiger auf einen vom Aufrufer zugeordneten Speicherpuffer der *Größe*.</span><span class="sxs-lookup"><span data-stu-id="107e0-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span>

</dd> <dt>

<span data-ttu-id="107e0-115">*length*</span><span class="sxs-lookup"><span data-stu-id="107e0-115">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="107e0-116">Länge des Speicherpuffers.</span><span class="sxs-lookup"><span data-stu-id="107e0-116">Length of the memory buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="107e0-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="107e0-117">Remarks</span></span>

<span data-ttu-id="107e0-118">Die Basisklasse ändert den im *phr-Parameter* übergebenen **HRESULT-Wert** nicht.</span><span class="sxs-lookup"><span data-stu-id="107e0-118">The base class does not modify the **HRESULT** value passed in the *phr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="107e0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="107e0-119">Requirements</span></span>



| <span data-ttu-id="107e0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="107e0-120">Requirement</span></span> | <span data-ttu-id="107e0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="107e0-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="107e0-122">Header</span><span class="sxs-lookup"><span data-stu-id="107e0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="107e0-123"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="107e0-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="107e0-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="107e0-124">Library</span></span><br/> | <dl> <span data-ttu-id="107e0-125"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="107e0-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="107e0-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="107e0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="107e0-127">**CMediaSample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="107e0-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




