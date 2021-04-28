---
description: 'CBaseInputPin.Inactive-Methode: Die Inaktive Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.'
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: CBaseInputPin.Inactive-Methode (Amfilter.h)
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
ms.openlocfilehash: 1324e9e2641e5e05bc3b0429ee269098c13d4bae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099728"
---
# <a name="cbaseinputpininactive-method"></a><span data-ttu-id="a8326-103">CBaseInputPin.Inactive-Methode</span><span class="sxs-lookup"><span data-stu-id="a8326-103">CBaseInputPin.Inactive method</span></span>

<span data-ttu-id="a8326-104">Die `Inactive` -Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="a8326-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8326-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8326-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="a8326-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8326-106">Parameters</span></span>

<span data-ttu-id="a8326-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a8326-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8326-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8326-108">Return value</span></span>

<span data-ttu-id="a8326-109">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="a8326-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a8326-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="a8326-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="a8326-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a8326-111">Return code</span></span>                                                                                          | <span data-ttu-id="a8326-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8326-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a8326-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a8326-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="a8326-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="a8326-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="a8326-115"><dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt></span><span class="sxs-lookup"><span data-stu-id="a8326-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="a8326-116">Es ist keine Speicherzuweisung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a8326-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a8326-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8326-117">Remarks</span></span>

<span data-ttu-id="a8326-118">Diese Methode überschreibt die [**CBasePin::Inactive-Methode.**](cbasepin-inactive.md)</span><span class="sxs-lookup"><span data-stu-id="a8326-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="a8326-119">Sie ruft die [**IMemAllocator::D ecommit-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) auf, um denCommit der Speicherbelegung zu decommitieren.</span><span class="sxs-lookup"><span data-stu-id="a8326-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="a8326-120">Wenn Sie diese Methode überschreiben, rufen Sie die Basisklassenmethode aus ihrer überschreibenden Methode auf.</span><span class="sxs-lookup"><span data-stu-id="a8326-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8326-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8326-121">Requirements</span></span>



| <span data-ttu-id="a8326-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8326-122">Requirement</span></span> | <span data-ttu-id="a8326-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a8326-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8326-124">Header</span><span class="sxs-lookup"><span data-stu-id="a8326-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a8326-125"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="a8326-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a8326-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8326-126">Library</span></span><br/> | <dl> <span data-ttu-id="a8326-127"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a8326-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8326-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a8326-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8326-129">**CBaseInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a8326-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




