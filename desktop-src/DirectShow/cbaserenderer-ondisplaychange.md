---
description: Die ondisplaychange-Methode stellt ein angezeigter EC- \_ Anzeige \_ Ereignis an den Filter Diagramm-Manager.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Cbaserenderer. ondisplaychange-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e99a8626d523e8b14b013acc9d2ead462f48df3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364543"
---
# <a name="cbaserendererondisplaychange-method"></a><span data-ttu-id="6267e-103">Cbaserenderer. ondisplaychange-Methode</span><span class="sxs-lookup"><span data-stu-id="6267e-103">CBaseRenderer.OnDisplayChange method</span></span>

<span data-ttu-id="6267e-104">Die-Methode stellt ein angezeigter `OnDisplayChange` [**EC- \_ Anzeige \_**](ec-display-changed.md) Ereignis an den Filter Diagramm-Manager.</span><span class="sxs-lookup"><span data-stu-id="6267e-104">The `OnDisplayChange` method posts an [**EC\_DISPLAY\_CHANGED**](ec-display-changed.md) event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="6267e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6267e-105">Syntax</span></span>


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a><span data-ttu-id="6267e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6267e-106">Parameters</span></span>

<span data-ttu-id="6267e-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6267e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6267e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6267e-108">Return value</span></span>

<span data-ttu-id="6267e-109">Gibt " **true** " zurück, wenn das Ereignis gepostet wurde, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="6267e-109">Returns **TRUE** if the event was posted, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6267e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6267e-110">Remarks</span></span>

<span data-ttu-id="6267e-111">Videorenderer sollten diese Methode als Reaktion auf WM \_ Display Change-Nachrichten aufruft.</span><span class="sxs-lookup"><span data-stu-id="6267e-111">Video renderers should call this method in response to WM\_DISPLAYCHANGE messages.</span></span> <span data-ttu-id="6267e-112">Wenn die eingabepin verbunden ist, sendet die Methode \_ ein \_ geändertes Ereignis der EC-Anzeige an den Filter Diagramm-Manager.</span><span class="sxs-lookup"><span data-stu-id="6267e-112">If the input pin is connected, the method sends an EC\_DISPLAY\_CHANGED event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="6267e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6267e-113">Requirements</span></span>



| <span data-ttu-id="6267e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6267e-114">Requirement</span></span> | <span data-ttu-id="6267e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6267e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6267e-116">Header</span><span class="sxs-lookup"><span data-stu-id="6267e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6267e-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6267e-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6267e-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6267e-118">Library</span></span><br/> | <dl> <span data-ttu-id="6267e-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6267e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6267e-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6267e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6267e-121">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6267e-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




