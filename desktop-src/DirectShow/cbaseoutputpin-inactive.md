---
description: 'CBaseOutputPin.Inactive-Methode: Die Inaktive Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.'
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: CBaseOutputPin.Inactive-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc4901bba7f1e34d49ff5bafb7b291544157bd9c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096138"
---
# <a name="cbaseoutputpininactive-method"></a><span data-ttu-id="4f9c3-103">CBaseOutputPin.Inactive-Methode</span><span class="sxs-lookup"><span data-stu-id="4f9c3-103">CBaseOutputPin.Inactive method</span></span>

<span data-ttu-id="4f9c3-104">Die `Inactive` -Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="4f9c3-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f9c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f9c3-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="4f9c3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f9c3-106">Parameters</span></span>

<span data-ttu-id="4f9c3-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4f9c3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f9c3-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f9c3-108">Return value</span></span>

<span data-ttu-id="4f9c3-109">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="4f9c3-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4f9c3-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="4f9c3-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="4f9c3-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4f9c3-111">Return code</span></span>                                                                                          | <span data-ttu-id="4f9c3-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f9c3-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4f9c3-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4f9c3-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="4f9c3-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="4f9c3-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="4f9c3-115"><dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt></span><span class="sxs-lookup"><span data-stu-id="4f9c3-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="4f9c3-116">Es ist keine Speicherzuweisung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f9c3-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f9c3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f9c3-117">Remarks</span></span>

<span data-ttu-id="4f9c3-118">Diese Methode überschreibt die [**CBasePin::Inactive-Methode.**](cbasepin-inactive.md)</span><span class="sxs-lookup"><span data-stu-id="4f9c3-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="4f9c3-119">Sie ruft die [**IMemAllocator::D ecommit-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) auf, um denCommit der Speicherbelegung zu decommitieren.</span><span class="sxs-lookup"><span data-stu-id="4f9c3-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="4f9c3-120">Wenn Sie diese Methode überschreiben, rufen Sie die Basisklassenmethode aus ihrer überschreibenden Methode auf.</span><span class="sxs-lookup"><span data-stu-id="4f9c3-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f9c3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f9c3-121">Requirements</span></span>



| <span data-ttu-id="4f9c3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f9c3-122">Requirement</span></span> | <span data-ttu-id="4f9c3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4f9c3-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f9c3-124">Header</span><span class="sxs-lookup"><span data-stu-id="4f9c3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4f9c3-125"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="4f9c3-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4f9c3-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4f9c3-126">Library</span></span><br/> | <dl> <span data-ttu-id="4f9c3-127"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4f9c3-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f9c3-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4f9c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f9c3-129">**CBaseOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4f9c3-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




