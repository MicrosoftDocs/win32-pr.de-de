---
description: Die getsetupdata-Methode ruft die Registrierungsdaten für den Filter ab.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Cbasefilter. getsetupdata-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367756"
---
# <a name="cbasefiltergetsetupdata-method"></a><span data-ttu-id="91f57-103">Cbasefilter. getsetupdata-Methode</span><span class="sxs-lookup"><span data-stu-id="91f57-103">CBaseFilter.GetSetupData method</span></span>

<span data-ttu-id="91f57-104">Die- `GetSetupData` Methode ruft die Registrierungsdaten für den Filter ab.</span><span class="sxs-lookup"><span data-stu-id="91f57-104">The `GetSetupData` method retrieves the registration data for the filter.</span></span>

> [!Note]  
> <span data-ttu-id="91f57-105">Diese Methode ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="91f57-105">This method is obsolete.</span></span> <span data-ttu-id="91f57-106">Sie wird von den Methoden [**cbasefilter:: Register**](cbasefilter-register.md) und [**cbasefilter:: unregister**](cbasefilter-unregister.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="91f57-106">It is called by the [**CBaseFilter::Register**](cbasefilter-register.md) and [**CBaseFilter::Unregister**](cbasefilter-unregister.md) methods.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="91f57-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="91f57-107">Syntax</span></span>


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a><span data-ttu-id="91f57-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="91f57-108">Parameters</span></span>

<span data-ttu-id="91f57-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="91f57-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91f57-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91f57-110">Return value</span></span>

<span data-ttu-id="91f57-111">Gibt einen Zeiger auf eine [**amoviesetup- \_ Filter**](amoviesetup-filter.md) Struktur zurück, die Registrierungsinformationen für den Filter enthält.</span><span class="sxs-lookup"><span data-stu-id="91f57-111">Returns a pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure containing registration information for the filter.</span></span>

## <a name="remarks"></a><span data-ttu-id="91f57-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91f57-112">Remarks</span></span>

<span data-ttu-id="91f57-113">Die Basisklasse gibt **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="91f57-113">The base class returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="91f57-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91f57-114">Requirements</span></span>



| <span data-ttu-id="91f57-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91f57-115">Requirement</span></span> | <span data-ttu-id="91f57-116">Wert</span><span class="sxs-lookup"><span data-stu-id="91f57-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91f57-117">Header</span><span class="sxs-lookup"><span data-stu-id="91f57-117">Header</span></span><br/>  | <dl> <span data-ttu-id="91f57-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91f57-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="91f57-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="91f57-119">Library</span></span><br/> | <dl> <span data-ttu-id="91f57-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="91f57-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91f57-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91f57-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91f57-122">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="91f57-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




