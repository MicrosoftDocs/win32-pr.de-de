---
description: Ein Zeiger auf die Zuweisung, die dieses Beispiel erstellt hat.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'Cmediasample:: m_pAllocator Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367555"
---
# <a name="cmediasamplem_pallocator-member"></a><span data-ttu-id="64db1-103">Cmediasample:: m \_ pallocator-Member</span><span class="sxs-lookup"><span data-stu-id="64db1-103">CMediaSample::m\_pAllocator member</span></span>

<span data-ttu-id="64db1-104">Ein Zeiger auf die Zuweisung, die dieses Beispiel erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="64db1-104">Pointer to the allocator that created this sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="64db1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64db1-105">Syntax</span></span>


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a><span data-ttu-id="64db1-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64db1-106">Remarks</span></span>

<span data-ttu-id="64db1-107">Obwohl das Beispiel einen Zeiger auf die Zuweisung beibehält, enthält es keinen Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="64db1-107">Although the sample keeps a pointer to the allocator, it does not hold a reference count.</span></span> <span data-ttu-id="64db1-108">Stattdessen erhöht die Zuweisung ihren eigenen Verweis Zähler in der [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Methode und gibt sich selbst in der [**imemzuzucator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) -Methode frei.</span><span class="sxs-lookup"><span data-stu-id="64db1-108">Instead, the allocator increments its own reference count in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method, and releases itself in the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span> <span data-ttu-id="64db1-109">Dadurch wird sichergestellt, dass die Zuweisung verfügbar ist, solange das Beispiel von einem anderen Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64db1-109">This guarantees that the allocator will be available as long as another object is using the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="64db1-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64db1-110">Requirements</span></span>



| <span data-ttu-id="64db1-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64db1-111">Requirement</span></span> | <span data-ttu-id="64db1-112">Wert</span><span class="sxs-lookup"><span data-stu-id="64db1-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64db1-113">Header</span><span class="sxs-lookup"><span data-stu-id="64db1-113">Header</span></span><br/>  | <dl> <span data-ttu-id="64db1-114"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64db1-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="64db1-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="64db1-115">Library</span></span><br/> | <dl> <span data-ttu-id="64db1-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="64db1-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64db1-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64db1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64db1-118">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="64db1-118">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




