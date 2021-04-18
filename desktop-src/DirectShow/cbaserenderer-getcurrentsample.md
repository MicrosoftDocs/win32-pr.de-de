---
description: Die getcurrentsample-Methode ruft das aktuelle Beispiel ab.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Cbaserderderer. getcurrentsample-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48c42ff02b22d30138fcad7d1e8af5e57a391b99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371173"
---
# <a name="cbaserenderergetcurrentsample-method"></a><span data-ttu-id="fb678-103">Cbaserderderer. getcurrentsample-Methode</span><span class="sxs-lookup"><span data-stu-id="fb678-103">CBaseRenderer.GetCurrentSample method</span></span>

<span data-ttu-id="fb678-104">Die- `GetCurrentSample` Methode ruft das aktuelle Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="fb678-104">The `GetCurrentSample` method retrieves the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb678-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb678-105">Syntax</span></span>


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a><span data-ttu-id="fb678-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb678-106">Parameters</span></span>

<span data-ttu-id="fb678-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fb678-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb678-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb678-108">Return value</span></span>

<span data-ttu-id="fb678-109">Gibt einen Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels zurück, oder **null** , wenn keine Stichprobe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fb678-109">Returns a pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface, or **NULL** if no sample is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb678-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb678-110">Remarks</span></span>

<span data-ttu-id="fb678-111">Wenn die Methode nicht **null** zurückgibt, ruft die Methode vor der Rückgabe die Methode " **adressf** " für den [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Zeiger auf.</span><span class="sxs-lookup"><span data-stu-id="fb678-111">Unless the method returns **NULL**, the method calls **AddRef** on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer before returning it.</span></span> <span data-ttu-id="fb678-112">Der Aufrufer muss den Zeiger freigeben.</span><span class="sxs-lookup"><span data-stu-id="fb678-112">The caller must release the pointer.</span></span> <span data-ttu-id="fb678-113">(Implizit müssen Sie den Rückgabewert einer Variablen zuweisen, damit Sie Sie später freigeben können.)</span><span class="sxs-lookup"><span data-stu-id="fb678-113">(By implication, you must assign the return value to a variable, so that you can release it later.)</span></span>

## <a name="requirements"></a><span data-ttu-id="fb678-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb678-114">Requirements</span></span>



| <span data-ttu-id="fb678-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb678-115">Requirement</span></span> | <span data-ttu-id="fb678-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fb678-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb678-117">Header</span><span class="sxs-lookup"><span data-stu-id="fb678-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fb678-118"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb678-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fb678-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb678-119">Library</span></span><br/> | <dl> <span data-ttu-id="fb678-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fb678-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb678-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb678-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb678-122">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fb678-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




