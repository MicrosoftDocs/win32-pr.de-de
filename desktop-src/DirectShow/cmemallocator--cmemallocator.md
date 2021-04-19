---
description: Dekonstruktormethode.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: Cmemzuordcator. ~ cmemzugerdebugtor (amfilter. h)
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
ms.openlocfilehash: d49046eccd8d7ef71c4eeb4c75acffbf90f7d826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369670"
---
# <a name="cmemallocatorcmemallocator-destructor"></a><span data-ttu-id="bc9e4-103">Cmemzuordcator. ~ cmemzugerdekonstruktor</span><span class="sxs-lookup"><span data-stu-id="bc9e4-103">CMemAllocator.~CMemAllocator destructor</span></span>

<span data-ttu-id="bc9e4-104">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="bc9e4-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc9e4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc9e4-105">Syntax</span></span>


```C++
~CMemAllocator();
```



## <a name="remarks"></a><span data-ttu-id="bc9e4-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc9e4-106">Remarks</span></span>

<span data-ttu-id="bc9e4-107">Diese Methode überschreibt den basisklassendekonstruktor zum Aufrufen von [**cbasezucator::D ecommit**](cbaseallocator-decommit.md) und [**cmemzucator:: reallyfree**](cmemallocator-reallyfree.md).</span><span class="sxs-lookup"><span data-stu-id="bc9e4-107">This method overrides the base-class destructor to call [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) and [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc9e4-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc9e4-108">Requirements</span></span>



| <span data-ttu-id="bc9e4-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc9e4-109">Requirement</span></span> | <span data-ttu-id="bc9e4-110">Wert</span><span class="sxs-lookup"><span data-stu-id="bc9e4-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc9e4-111">Header</span><span class="sxs-lookup"><span data-stu-id="bc9e4-111">Header</span></span><br/>  | <dl> <span data-ttu-id="bc9e4-112"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc9e4-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bc9e4-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bc9e4-113">Library</span></span><br/> | <dl> <span data-ttu-id="bc9e4-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bc9e4-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc9e4-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc9e4-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc9e4-116">**Cmemzuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bc9e4-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




