---
description: CBaseAllocator.~CBaseAllocator-Destruktor – Destruktormethode.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: CBaseAllocator.~CBaseAllocator-Destruktor (Amfilter.h)
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
ms.openlocfilehash: 9a4b754c8937b87a547f4583b3270f5782a6a415
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096418"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="46058-103">CBaseAllocator.~CBaseAllocator-Destruktor</span><span class="sxs-lookup"><span data-stu-id="46058-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="46058-104">Destruktormethode.</span><span class="sxs-lookup"><span data-stu-id="46058-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="46058-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46058-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="46058-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46058-106">Remarks</span></span>

<span data-ttu-id="46058-107">Rufen Sie immer [**die CBaseAllocator::D commit-Methode auf,**](cbaseallocator-decommit.md) bevor Sie das Objekt zerstören.</span><span class="sxs-lookup"><span data-stu-id="46058-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="46058-108">Der Basisklassen-Destruktor kann **decommit** nicht aufrufen, da diese Methode die reine virtuelle [**Methode CBaseAllocator::Free aufruft.**](cbaseallocator-free.md)</span><span class="sxs-lookup"><span data-stu-id="46058-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="46058-109">Abgeleitete Klassen sollten diesen Destruktor überschreiben und **Decommit aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="46058-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="46058-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46058-110">Requirements</span></span>



| <span data-ttu-id="46058-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46058-111">Requirement</span></span> | <span data-ttu-id="46058-112">Wert</span><span class="sxs-lookup"><span data-stu-id="46058-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46058-113">Header</span><span class="sxs-lookup"><span data-stu-id="46058-113">Header</span></span><br/>  | <dl> <span data-ttu-id="46058-114"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="46058-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="46058-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="46058-115">Library</span></span><br/> | <dl> <span data-ttu-id="46058-116"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="46058-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46058-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="46058-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46058-118">**CBaseAllocator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="46058-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




