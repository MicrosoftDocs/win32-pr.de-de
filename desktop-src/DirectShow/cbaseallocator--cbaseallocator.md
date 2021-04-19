---
description: Dekonstruktormethode.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: Cbasezucator. ~ cbasezucator-debugtor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364030"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="786e0-103">Cbasezucator. ~ cbasezuweisung-Dekonstruktor</span><span class="sxs-lookup"><span data-stu-id="786e0-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="786e0-104">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="786e0-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="786e0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="786e0-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="786e0-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="786e0-106">Remarks</span></span>

<span data-ttu-id="786e0-107">Immer die [**cbasezucator::D ecommit**](cbaseallocator-decommit.md) -Methode aufruft, bevor das Objekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="786e0-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="786e0-108">Der basisklassendekonstruktor kann " **Decommit**" nicht aufrufen, da diese Methode die rein virtuelle Methode " [**cbasezucator:: Free**](cbaseallocator-free.md)" aufruft.</span><span class="sxs-lookup"><span data-stu-id="786e0-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="786e0-109">Abgeleitete Klassen sollten diesen Dekonstruktor überschreiben und **Decommit** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="786e0-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="786e0-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="786e0-110">Requirements</span></span>



| <span data-ttu-id="786e0-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="786e0-111">Requirement</span></span> | <span data-ttu-id="786e0-112">Wert</span><span class="sxs-lookup"><span data-stu-id="786e0-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="786e0-113">Header</span><span class="sxs-lookup"><span data-stu-id="786e0-113">Header</span></span><br/>  | <dl> <span data-ttu-id="786e0-114"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="786e0-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="786e0-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="786e0-115">Library</span></span><br/> | <dl> <span data-ttu-id="786e0-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="786e0-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="786e0-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="786e0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="786e0-118">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="786e0-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




