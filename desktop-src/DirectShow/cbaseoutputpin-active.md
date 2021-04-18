---
description: Die aktive Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Cbaseoutputpin. Active-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 249cddac4027fa434996b1118cc692937b686a83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365496"
---
# <a name="cbaseoutputpinactive-method"></a><span data-ttu-id="ed90e-103">Cbaseoutputpin. Active-Methode</span><span class="sxs-lookup"><span data-stu-id="ed90e-103">CBaseOutputPin.Active method</span></span>

<span data-ttu-id="ed90e-104">Die- `Active` Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="ed90e-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed90e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed90e-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="ed90e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed90e-106">Parameters</span></span>

<span data-ttu-id="ed90e-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ed90e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed90e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed90e-108">Return value</span></span>

<span data-ttu-id="ed90e-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ed90e-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ed90e-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="ed90e-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="ed90e-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ed90e-111">Return code</span></span>                                                                                          | <span data-ttu-id="ed90e-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed90e-112">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ed90e-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ed90e-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="ed90e-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ed90e-114">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="ed90e-115"><dt>**VFW \_ E \_ No- \_ Zuweisung**</dt></span><span class="sxs-lookup"><span data-stu-id="ed90e-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="ed90e-116">Es ist keine Zuweisung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ed90e-116">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ed90e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed90e-117">Remarks</span></span>

<span data-ttu-id="ed90e-118">Diese Methode überschreibt die [**cbasepin:: Active**](cbasepin-active.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ed90e-118">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="ed90e-119">Es wird die [**imemallocator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) -Methode für die Zuweisung aufgerufen, um Speicher für Puffer zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ed90e-119">It calls the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method on the allocator, to allocate memory for buffers.</span></span>

<span data-ttu-id="ed90e-120">Wenn Sie diese Methode überschreiben, müssen Sie die Basisklassen Methode aus der über schreibenden Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="ed90e-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed90e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed90e-121">Requirements</span></span>



| <span data-ttu-id="ed90e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed90e-122">Requirement</span></span> | <span data-ttu-id="ed90e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ed90e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed90e-124">Header</span><span class="sxs-lookup"><span data-stu-id="ed90e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ed90e-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed90e-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ed90e-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ed90e-126">Library</span></span><br/> | <dl> <span data-ttu-id="ed90e-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ed90e-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed90e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed90e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed90e-129">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ed90e-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




