---
description: 'CBaseInputPin.BreakConnect-Methode: Die BreakConnect-Methode gibt den Pin von einer Verbindung frei.'
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: CBaseInputPin.BreakConnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5398f675e056da2c60747c0b4eb17c475771bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099738"
---
# <a name="cbaseinputpinbreakconnect-method"></a><span data-ttu-id="dbded-103">CBaseInputPin.BreakConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="dbded-103">CBaseInputPin.BreakConnect method</span></span>

<span data-ttu-id="dbded-104">Die `BreakConnect` -Methode gibt den Pin von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="dbded-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbded-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbded-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="dbded-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbded-106">Parameters</span></span>

<span data-ttu-id="dbded-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="dbded-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dbded-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbded-108">Return value</span></span>

<span data-ttu-id="dbded-109">Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="dbded-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbded-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbded-110">Remarks</span></span>

<span data-ttu-id="dbded-111">Diese Methode überschreibt die [**CBasePin::BreakConnect-Methode.**](cbasepin-breakconnect.md)</span><span class="sxs-lookup"><span data-stu-id="dbded-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="dbded-112">Er dekommitiert die Zuweisung und gibt die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) frei.</span><span class="sxs-lookup"><span data-stu-id="dbded-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="dbded-113">Wenn Sie diese Methode überschreiben, rufen Sie die Basisklassenmethode aus Ihrer überschreibenden Methode auf.</span><span class="sxs-lookup"><span data-stu-id="dbded-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="dbded-114">Andernfalls können Speicherverluste entstehen.</span><span class="sxs-lookup"><span data-stu-id="dbded-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbded-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbded-115">Requirements</span></span>



| <span data-ttu-id="dbded-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbded-116">Requirement</span></span> | <span data-ttu-id="dbded-117">Wert</span><span class="sxs-lookup"><span data-stu-id="dbded-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbded-118">Header</span><span class="sxs-lookup"><span data-stu-id="dbded-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dbded-119"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="dbded-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dbded-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dbded-120">Library</span></span><br/> | <dl> <span data-ttu-id="dbded-121"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="dbded-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbded-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dbded-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbded-123">**CBaseInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dbded-123">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




