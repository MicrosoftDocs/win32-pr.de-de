---
description: Die resetendof Stream-Methode setzt die Flags für das Ende des Streams zurück.
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: Cbaserderderer. rectendof Stream-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0269ee2dfafea9265b5eeb82caa4c39f8d91320c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371351"
---
# <a name="cbaserendererresetendofstream-method"></a><span data-ttu-id="7706f-103">Cbaserderderer. rectendof Stream-Methode</span><span class="sxs-lookup"><span data-stu-id="7706f-103">CBaseRenderer.ResetEndOfStream method</span></span>

<span data-ttu-id="7706f-104">Die `ResetEndOfStream` -Methode setzt die Flags für das Ende des Streams zurück.</span><span class="sxs-lookup"><span data-stu-id="7706f-104">The `ResetEndOfStream` method resets the end-of-stream flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="7706f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7706f-105">Syntax</span></span>


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="7706f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7706f-106">Parameters</span></span>

<span data-ttu-id="7706f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7706f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7706f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7706f-108">Return value</span></span>

<span data-ttu-id="7706f-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="7706f-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7706f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7706f-110">Remarks</span></span>

<span data-ttu-id="7706f-111">Diese Methode löscht die vorherige Bedingung für das Ende des Streams.</span><span class="sxs-lookup"><span data-stu-id="7706f-111">This method clears the previous end-of-stream condition.</span></span> <span data-ttu-id="7706f-112">An diesem Punkt kann der Filter neue Daten empfangen.</span><span class="sxs-lookup"><span data-stu-id="7706f-112">At that point, the filter can receive new data.</span></span> <span data-ttu-id="7706f-113">Die [**cbaserenderer::**](cbaserenderer-stop.md) und [**cbaserenderer:: beginflush**](cbaserenderer-beginflush.md) -Methoden aufrufen diese Methode.</span><span class="sxs-lookup"><span data-stu-id="7706f-113">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7706f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7706f-114">Requirements</span></span>



| <span data-ttu-id="7706f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7706f-115">Requirement</span></span> | <span data-ttu-id="7706f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7706f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7706f-117">Header</span><span class="sxs-lookup"><span data-stu-id="7706f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7706f-118"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7706f-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7706f-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7706f-119">Library</span></span><br/> | <dl> <span data-ttu-id="7706f-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7706f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7706f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7706f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7706f-122">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7706f-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




