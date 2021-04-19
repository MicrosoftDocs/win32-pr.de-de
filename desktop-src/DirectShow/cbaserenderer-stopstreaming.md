---
description: Die stopstreaming-Methode stoppt das Streaming, wenn der Filter den Status "wird ausgeführt" verlässt.
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: Cbaserderderer. stopstreaming-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfd943de6a53383d7505fa9e884dcc152da6e5f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367180"
---
# <a name="cbaserendererstopstreaming-method"></a><span data-ttu-id="d797c-103">Cbaserderderer. stopstreaming-Methode</span><span class="sxs-lookup"><span data-stu-id="d797c-103">CBaseRenderer.StopStreaming method</span></span>

<span data-ttu-id="d797c-104">Die- `StopStreaming` Methode stoppt das Streaming, wenn der Filter den Status "wird ausgeführt" verlässt.</span><span class="sxs-lookup"><span data-stu-id="d797c-104">The `StopStreaming` method halts streaming when the filter switches out of the running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="d797c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d797c-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="d797c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d797c-106">Parameters</span></span>

<span data-ttu-id="d797c-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d797c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d797c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d797c-108">Return value</span></span>

<span data-ttu-id="d797c-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="d797c-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d797c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d797c-110">Remarks</span></span>

<span data-ttu-id="d797c-111">Diese Methode ruft die [**cbaserdenderer:: onstopstreaming**](cbaserenderer-onstopstreaming.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="d797c-111">This method calls the [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md) method.</span></span> <span data-ttu-id="d797c-112">Diese Methode führt in der Basisklasse keine Aktion aus, die abgeleitete Klasse kann Sie jedoch überschreiben.</span><span class="sxs-lookup"><span data-stu-id="d797c-112">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d797c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d797c-113">Requirements</span></span>



| <span data-ttu-id="d797c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d797c-114">Requirement</span></span> | <span data-ttu-id="d797c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d797c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d797c-116">Header</span><span class="sxs-lookup"><span data-stu-id="d797c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d797c-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d797c-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d797c-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d797c-118">Library</span></span><br/> | <dl> <span data-ttu-id="d797c-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d797c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d797c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d797c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d797c-121">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d797c-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




