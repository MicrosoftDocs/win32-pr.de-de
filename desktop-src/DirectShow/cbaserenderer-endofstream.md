---
description: Die EndOfStream-Methode benachrichtigt den Filter, dass die Eingabe-PIN eine Benachrichtigung über das Ende des Datenstroms erhalten hat.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Cbaserderderer. EndOf Stream-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364762"
---
# <a name="cbaserendererendofstream-method"></a><span data-ttu-id="910f6-103">Cbaserderderer. EndOf Stream-Methode</span><span class="sxs-lookup"><span data-stu-id="910f6-103">CBaseRenderer.EndOfStream method</span></span>

<span data-ttu-id="910f6-104">Die- `EndOfStream` Methode benachrichtigt den Filter, dass die Eingabe-PIN eine Benachrichtigung über das Ende des Datenstroms erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="910f6-104">The `EndOfStream` method notifies the filter that the input pin received an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="910f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="910f6-105">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="910f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="910f6-106">Parameters</span></span>

<span data-ttu-id="910f6-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="910f6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="910f6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="910f6-108">Return value</span></span>

<span data-ttu-id="910f6-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="910f6-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="910f6-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="910f6-110">Remarks</span></span>

<span data-ttu-id="910f6-111">Die Eingabe-PIN des Filters ruft diese Methode auf, wenn Sie eine Benachrichtigung über das Ende des Datenstroms empfängt.</span><span class="sxs-lookup"><span data-stu-id="910f6-111">The filter's input pin calls this method when it receives an end-of-stream notification.</span></span>

<span data-ttu-id="910f6-112">Diese Methode legt das Flag " [**cbaserrederer:: m \_ BeOS**](cbaserenderer-m-beos.md) " auf " **true** " fest und ruft die [**cbasererentiderer:: sendendofstream**](cbaserenderer-sendendofstream.md) -Methode auf, um ein [**EC \_ Complete**](ec-complete.md) -Ereignis zu planen.</span><span class="sxs-lookup"><span data-stu-id="910f6-112">This method sets the [**CBaseRenderer::m\_bEOS**](cbaserenderer-m-beos.md) flag to **TRUE** and calls the [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method to schedule an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="910f6-113">Wenn der Filter angehalten wurde und auf eine Stichprobe wartet, schließt diese Methode den Zustandsübergang ab.</span><span class="sxs-lookup"><span data-stu-id="910f6-113">If the filter is paused and waiting for a sample, this method completes the state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="910f6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="910f6-114">Requirements</span></span>



| <span data-ttu-id="910f6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="910f6-115">Requirement</span></span> | <span data-ttu-id="910f6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="910f6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="910f6-117">Header</span><span class="sxs-lookup"><span data-stu-id="910f6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="910f6-118"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="910f6-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="910f6-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="910f6-119">Library</span></span><br/> | <dl> <span data-ttu-id="910f6-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="910f6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="910f6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="910f6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="910f6-122">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="910f6-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




