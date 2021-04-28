---
description: 'CBaseOutputPin.EndFlush-Methode: Die EndFlush-Methode beendet einen Leerungsvorgang. Diese Methode implementiert die IPin::EndFlush-Methode.'
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: CBaseOutputPin.EndFlush-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53153c6dbd941390c7ef616ee36c56e01214c341
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099508"
---
# <a name="cbaseoutputpinendflush-method"></a><span data-ttu-id="b3432-104">CBaseOutputPin.EndFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="b3432-104">CBaseOutputPin.EndFlush method</span></span>

<span data-ttu-id="b3432-105">Die `EndFlush` -Methode beendet einen Leerungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="b3432-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="b3432-106">Diese Methode implementiert die [**IPin::EndFlush-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)</span><span class="sxs-lookup"><span data-stu-id="b3432-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3432-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3432-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="b3432-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3432-108">Parameters</span></span>

<span data-ttu-id="b3432-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b3432-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3432-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3432-110">Return value</span></span>

<span data-ttu-id="b3432-111">Gibt E \_ UNEXPECTED zurück.</span><span class="sxs-lookup"><span data-stu-id="b3432-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3432-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3432-112">Remarks</span></span>

<span data-ttu-id="b3432-113">Diese Methode sollte nur für Eingabepins aufgerufen werden, sodass die **CBaseOutputPin-Implementierung** E \_ UNEXPECTED zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b3432-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3432-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3432-114">Requirements</span></span>



| <span data-ttu-id="b3432-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3432-115">Requirement</span></span> | <span data-ttu-id="b3432-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b3432-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3432-117">Header</span><span class="sxs-lookup"><span data-stu-id="b3432-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b3432-118"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b3432-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b3432-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3432-119">Library</span></span><br/> | <dl> <span data-ttu-id="b3432-120"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b3432-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3432-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b3432-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3432-122">**CBaseOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b3432-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




