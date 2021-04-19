---
description: Die getpincount-Methode ruft die Anzahl der Pins ab.
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Cbasefilter. getpincount-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8da1cbc22a49b149bdccc36c3b854b44101b9bbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366842"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="2ed7b-103">Cbasefilter. getpincount-Methode</span><span class="sxs-lookup"><span data-stu-id="2ed7b-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="2ed7b-104">Die- `GetPinCount` Methode ruft die Anzahl der Pins ab.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ed7b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ed7b-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="2ed7b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ed7b-106">Parameters</span></span>

<span data-ttu-id="2ed7b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ed7b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ed7b-108">Return value</span></span>

<span data-ttu-id="2ed7b-109">Gibt die Anzahl der Pins zurück.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ed7b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ed7b-110">Remarks</span></span>

<span data-ttu-id="2ed7b-111">Diese reine virtuelle Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="2ed7b-112">Gibt die Anzahl der Pins zurück, die zurzeit für diesen Filter verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="2ed7b-113">Filter können Pins dynamisch erstellen oder zerstören.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ed7b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ed7b-114">Requirements</span></span>



| <span data-ttu-id="2ed7b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ed7b-115">Requirement</span></span> | <span data-ttu-id="2ed7b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2ed7b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed7b-117">Header</span><span class="sxs-lookup"><span data-stu-id="2ed7b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2ed7b-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ed7b-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2ed7b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ed7b-119">Library</span></span><br/> | <dl> <span data-ttu-id="2ed7b-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2ed7b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ed7b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ed7b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ed7b-122">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2ed7b-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




