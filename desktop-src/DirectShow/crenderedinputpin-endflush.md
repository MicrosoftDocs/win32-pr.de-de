---
description: 'Die endflush-Methode beendet einen Löschvorgang. Diese Methode implementiert die IPin:: endflush-Methode.'
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Crenderedinputpin. endflush-Methode (amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d80f6cbc31a8bc5bf797847465a218f32631c1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368485"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="f8e1c-104">Crenderedinputpin. endflush-Methode</span><span class="sxs-lookup"><span data-stu-id="f8e1c-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="f8e1c-105">Die- `EndFlush` Methode beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="f8e1c-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="f8e1c-106">Diese Methode implementiert die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f8e1c-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e1c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8e1c-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="f8e1c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8e1c-108">Parameters</span></span>

<span data-ttu-id="f8e1c-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f8e1c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8e1c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8e1c-110">Return value</span></span>

<span data-ttu-id="f8e1c-111">Gibt \_ bei Erfolg S OK oder andernfalls einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="f8e1c-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8e1c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8e1c-112">Remarks</span></span>

<span data-ttu-id="f8e1c-113">Diese Methode löscht alle ausstehenden [**EC \_ Complete**](ec-complete.md) -Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="f8e1c-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8e1c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8e1c-114">Requirements</span></span>



| <span data-ttu-id="f8e1c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8e1c-115">Requirement</span></span> | <span data-ttu-id="f8e1c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f8e1c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e1c-117">Header</span><span class="sxs-lookup"><span data-stu-id="f8e1c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f8e1c-118"><dt>Amextra. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8e1c-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f8e1c-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f8e1c-119">Library</span></span><br/> | <dl> <span data-ttu-id="f8e1c-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f8e1c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8e1c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8e1c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8e1c-122">**Crenderedinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f8e1c-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




