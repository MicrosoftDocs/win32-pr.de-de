---
description: CMemAllocator.~CMemAllocator-Destruktor – Destruktormethode.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: CMemAllocator.~CMemAllocator-Destruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43b0505ee34df72ab82e4204b08440ac1a2558b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095408"
---
# <a name="cmemallocatorcmemallocator-destructor"></a><span data-ttu-id="c0f08-103">CMemAllocator.~CMemAllocator-Destruktor</span><span class="sxs-lookup"><span data-stu-id="c0f08-103">CMemAllocator.~CMemAllocator destructor</span></span>

<span data-ttu-id="c0f08-104">Destruktormethode.</span><span class="sxs-lookup"><span data-stu-id="c0f08-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f08-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0f08-105">Syntax</span></span>


```C++
~CMemAllocator();
```



## <a name="remarks"></a><span data-ttu-id="c0f08-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0f08-106">Remarks</span></span>

<span data-ttu-id="c0f08-107">Diese Methode überschreibt den Basisklassen-Destruktor, um [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) und [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c0f08-107">This method overrides the base-class destructor to call [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) and [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0f08-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0f08-108">Requirements</span></span>



| <span data-ttu-id="c0f08-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0f08-109">Requirement</span></span> | <span data-ttu-id="c0f08-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c0f08-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f08-111">Header</span><span class="sxs-lookup"><span data-stu-id="c0f08-111">Header</span></span><br/>  | <dl> <span data-ttu-id="c0f08-112"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c0f08-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c0f08-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c0f08-113">Library</span></span><br/> | <dl> <span data-ttu-id="c0f08-114"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c0f08-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f08-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c0f08-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f08-116">**CMemAllocator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c0f08-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




