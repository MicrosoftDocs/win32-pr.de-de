---
description: Die joinfiltergraph-Methode sendet \_ eine Ereignis Benachrichtigung für das EC-Fenster, \_ Wenn ein Filter aus dem Filter Diagramm entfernt wird.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Cbasevideorenderer. joinfiltergraph-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acabb6deeb6577fa04479fc4014e210d4a5654d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365680"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a><span data-ttu-id="d2f4c-103">Cbasevideorenderer. joinfiltergraph-Methode</span><span class="sxs-lookup"><span data-stu-id="d2f4c-103">CBaseVideoRenderer.JoinFilterGraph method</span></span>

<span data-ttu-id="d2f4c-104">Die- `JoinFilterGraph` Methode sendet eine Ereignis Benachrichtigung für das [**EC- \_ \_ Fenster**](ec-window-destroyed.md) , wenn ein Filter aus dem Filter Diagramm entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-104">The `JoinFilterGraph` method sends [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification when a filter is removed from the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f4c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2f4c-105">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="d2f4c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2f4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2f4c-107">*PGraph*</span><span class="sxs-lookup"><span data-stu-id="d2f4c-107">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="d2f4c-108">Zeiger auf das Filter Diagramm, das verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-108">Pointer to the filter graph to join.</span></span>

</dd> <dt>

<span data-ttu-id="d2f4c-109">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2f4c-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f4c-110">Zeiger auf den Namen des hinzugefügten Filters.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-110">Pointer to the name of the filter being added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2f4c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2f4c-111">Return value</span></span>

<span data-ttu-id="d2f4c-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2f4c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2f4c-113">Remarks</span></span>

<span data-ttu-id="d2f4c-114">Diese Member-Funktion überschreibt die [**cbasefilter:: joinfiltergraph**](cbasefilter-joinfiltergraph.md) -Member-Funktion.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-114">This member function overrides the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) member function.</span></span> <span data-ttu-id="d2f4c-115">Wenn der Filter das Filter Diagramm verlässt (*PGraph* ist **null**), wird eine Ereignis Benachrichtigung für ein [**EC- \_ Fenster \_**](ec-window-destroyed.md) gesendet, sodass der Ressourcen-Manager den Renderer nicht als Fokus Objekt speichert.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-115">If the filter is leaving the filter graph (*pGraph* is **NULL**), it sends an [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification so that the resource manager does not hold on to the renderer as a focus object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f4c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2f4c-116">Requirements</span></span>



| <span data-ttu-id="d2f4c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2f4c-117">Requirement</span></span> | <span data-ttu-id="d2f4c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d2f4c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f4c-119">Header</span><span class="sxs-lookup"><span data-stu-id="d2f4c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d2f4c-120"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2f4c-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d2f4c-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d2f4c-121">Library</span></span><br/> | <dl> <span data-ttu-id="d2f4c-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d2f4c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2f4c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2f4c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f4c-124">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d2f4c-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




