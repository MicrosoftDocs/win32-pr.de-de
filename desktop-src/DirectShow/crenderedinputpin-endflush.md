---
description: 'CRenderedInputPin.EndFlush-Methode: Die EndFlush-Methode beendet einen Leerungsvorgang. Diese Methode implementiert die IPin::EndFlush-Methode.'
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: CRenderedInputPin.EndFlush-Methode (Amextra.h)
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
ms.openlocfilehash: 7be740df2b3b45d0b681a86b8f70bed8e1395e8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098918"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="72ac6-104">CRenderedInputPin.EndFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="72ac6-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="72ac6-105">Die `EndFlush` -Methode beendet einen Leerungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="72ac6-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="72ac6-106">Diese Methode implementiert die [**IPin::EndFlush-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)</span><span class="sxs-lookup"><span data-stu-id="72ac6-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="72ac6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="72ac6-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="72ac6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="72ac6-108">Parameters</span></span>

<span data-ttu-id="72ac6-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="72ac6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72ac6-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72ac6-110">Return value</span></span>

<span data-ttu-id="72ac6-111">Gibt S \_ OK zurück, wenn erfolgreich, oder andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="72ac6-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="72ac6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72ac6-112">Remarks</span></span>

<span data-ttu-id="72ac6-113">Diese Methode löscht alle ausstehenden [**EC \_ COMPLETE-Ereignisse.**](ec-complete.md)</span><span class="sxs-lookup"><span data-stu-id="72ac6-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="72ac6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72ac6-114">Requirements</span></span>



| <span data-ttu-id="72ac6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72ac6-115">Requirement</span></span> | <span data-ttu-id="72ac6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="72ac6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72ac6-117">Header</span><span class="sxs-lookup"><span data-stu-id="72ac6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="72ac6-118"><dt>Amextra.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="72ac6-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="72ac6-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="72ac6-119">Library</span></span><br/> | <dl> <span data-ttu-id="72ac6-120"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="72ac6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72ac6-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="72ac6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ac6-122">**CRenderedInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="72ac6-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




