---
description: 'CBaseOutputPin.Active-Methode: Die Active-Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist.'
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: CBaseOutputPin.Active-Methode (Amfilter.h)
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
ms.openlocfilehash: f282f45bb895a941c44cb70cf5d9d3d373bf8649
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096208"
---
# <a name="cbaseoutputpinactive-method"></a><span data-ttu-id="3aa40-103">CBaseOutputPin.Active-Methode</span><span class="sxs-lookup"><span data-stu-id="3aa40-103">CBaseOutputPin.Active method</span></span>

<span data-ttu-id="3aa40-104">Die `Active` -Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="3aa40-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa40-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3aa40-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="3aa40-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3aa40-106">Parameters</span></span>

<span data-ttu-id="3aa40-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3aa40-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3aa40-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3aa40-108">Return value</span></span>

<span data-ttu-id="3aa40-109">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="3aa40-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3aa40-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="3aa40-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="3aa40-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3aa40-111">Return code</span></span>                                                                                          | <span data-ttu-id="3aa40-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3aa40-112">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3aa40-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3aa40-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="3aa40-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3aa40-114">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="3aa40-115"><dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt></span><span class="sxs-lookup"><span data-stu-id="3aa40-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="3aa40-116">Es ist keine Zuweisung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3aa40-116">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3aa40-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3aa40-117">Remarks</span></span>

<span data-ttu-id="3aa40-118">Diese Methode überschreibt die [**CBasePin::Active-Methode.**](cbasepin-active.md)</span><span class="sxs-lookup"><span data-stu-id="3aa40-118">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="3aa40-119">Sie ruft die [**IMemAllocator::Commit-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) für die Zuweisung auf, um Speicher für Puffer zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="3aa40-119">It calls the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method on the allocator, to allocate memory for buffers.</span></span>

<span data-ttu-id="3aa40-120">Wenn Sie diese Methode überschreiben, rufen Sie die Basisklassenmethode aus ihrer überschreibenden Methode auf.</span><span class="sxs-lookup"><span data-stu-id="3aa40-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa40-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3aa40-121">Requirements</span></span>



| <span data-ttu-id="3aa40-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3aa40-122">Requirement</span></span> | <span data-ttu-id="3aa40-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3aa40-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa40-124">Header</span><span class="sxs-lookup"><span data-stu-id="3aa40-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3aa40-125"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="3aa40-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3aa40-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3aa40-126">Library</span></span><br/> | <dl> <span data-ttu-id="3aa40-127"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3aa40-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa40-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3aa40-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa40-129">**CBaseOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3aa40-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




