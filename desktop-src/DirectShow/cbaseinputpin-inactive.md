---
description: Die inaktive Methode benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: Cbasinputpin. inaktive Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52bf7efa352e8a73d562c61c3833a051ee860d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369600"
---
# <a name="cbaseinputpininactive-method"></a><span data-ttu-id="6f20e-103">Cbasinputpin. inaktive Methode</span><span class="sxs-lookup"><span data-stu-id="6f20e-103">CBaseInputPin.Inactive method</span></span>

<span data-ttu-id="6f20e-104">Die- `Inactive` Methode benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="6f20e-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f20e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f20e-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="6f20e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f20e-106">Parameters</span></span>

<span data-ttu-id="6f20e-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6f20e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f20e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f20e-108">Return value</span></span>

<span data-ttu-id="6f20e-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6f20e-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6f20e-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="6f20e-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="6f20e-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6f20e-111">Return code</span></span>                                                                                          | <span data-ttu-id="6f20e-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f20e-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6f20e-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6f20e-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="6f20e-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="6f20e-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="6f20e-115"><dt>**VFW \_ E \_ No- \_ Zuweisung**</dt></span><span class="sxs-lookup"><span data-stu-id="6f20e-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="6f20e-116">Es ist keine Speicherzuweisung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6f20e-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6f20e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f20e-117">Remarks</span></span>

<span data-ttu-id="6f20e-118">Diese Methode überschreibt die [**cbasepin:: inaktive**](cbasepin-inactive.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6f20e-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="6f20e-119">Sie ruft die [**imemzuzucator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) -Methode auf, um die Speicher Belegung zu Decommit.</span><span class="sxs-lookup"><span data-stu-id="6f20e-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="6f20e-120">Wenn Sie diese Methode überschreiben, müssen Sie die Basisklassen Methode aus der über schreibenden Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="6f20e-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f20e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f20e-121">Requirements</span></span>



| <span data-ttu-id="6f20e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f20e-122">Requirement</span></span> | <span data-ttu-id="6f20e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6f20e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f20e-124">Header</span><span class="sxs-lookup"><span data-stu-id="6f20e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6f20e-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f20e-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6f20e-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6f20e-126">Library</span></span><br/> | <dl> <span data-ttu-id="6f20e-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6f20e-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f20e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f20e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f20e-129">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6f20e-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




