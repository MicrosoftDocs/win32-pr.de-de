---
description: 'Die beginflush-Methode startet einen Löschvorgang. Implementiert die IPin:: beginflush-Methode.'
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Cbaseoutputpin. beginflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0216f74094d0c024d9b354dc594ff8d65315efbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371178"
---
# <a name="cbaseoutputpinbeginflush-method"></a><span data-ttu-id="a6890-104">Cbaseoutputpin. beginflush-Methode</span><span class="sxs-lookup"><span data-stu-id="a6890-104">CBaseOutputPin.BeginFlush method</span></span>

<span data-ttu-id="a6890-105">Die- `BeginFlush` Methode startet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="a6890-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="a6890-106">Implementiert die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a6890-106">Implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6890-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6890-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="a6890-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6890-108">Parameters</span></span>

<span data-ttu-id="a6890-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a6890-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a6890-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6890-110">Return value</span></span>

<span data-ttu-id="a6890-111">Gibt "E unerwartete" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="a6890-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6890-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6890-112">Remarks</span></span>

<span data-ttu-id="a6890-113">Diese Methode sollte nur für Eingabe Pins aufgerufen werden, sodass die **cbaseoutputpin** -Implementierung E \_ unerwartet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a6890-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6890-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6890-114">Requirements</span></span>



| <span data-ttu-id="a6890-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6890-115">Requirement</span></span> | <span data-ttu-id="a6890-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a6890-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6890-117">Header</span><span class="sxs-lookup"><span data-stu-id="a6890-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a6890-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6890-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a6890-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a6890-119">Library</span></span><br/> | <dl> <span data-ttu-id="a6890-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a6890-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6890-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6890-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6890-122">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a6890-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




