---
description: Die getminidealimagesize-Methode ruft die minimale ideale Bildgröße ab.
ms.assetid: f2f2d10e-ee2c-4f8a-91ce-576319038e0d
title: Cbasecontrolwindow. getminidealimagesize-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMinIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24eeb4cdb5972f81e6dd66a812c9a38b61dcab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352989"
---
# <a name="cbasecontrolwindowgetminidealimagesize-method"></a><span data-ttu-id="e0fea-103">Cbasecontrolwindow. getminidealimagesize-Methode</span><span class="sxs-lookup"><span data-stu-id="e0fea-103">CBaseControlWindow.GetMinIdealImageSize method</span></span>

<span data-ttu-id="e0fea-104">Die- `GetMinIdealImageSize` Methode ruft die minimale ideale Bildgröße ab.</span><span class="sxs-lookup"><span data-stu-id="e0fea-104">The `GetMinIdealImageSize` method retrieves the minimum ideal image size.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0fea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0fea-105">Syntax</span></span>


```C++
HRESULT GetMinIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="e0fea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0fea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0fea-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="e0fea-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="e0fea-108">Zeiger auf die minimale ideale Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e0fea-108">Pointer to the minimum ideal width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e0fea-109">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="e0fea-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="e0fea-110">Zeiger auf die minimale ideale Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e0fea-110">Pointer to the minimum ideal height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0fea-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0fea-111">Return value</span></span>

<span data-ttu-id="e0fea-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e0fea-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0fea-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0fea-113">Remarks</span></span>

<span data-ttu-id="e0fea-114">Verschiedene Renderer haben Leistungsbeschränkungen hinsichtlich der Größe von Bildern, die Sie anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="e0fea-114">Various renderers have performance restrictions on the size of images they can display.</span></span> <span data-ttu-id="e0fea-115">Obwohl Sie weiterhin ordnungsgemäß funktionieren, wenn Sie aufgefordert werden, Bilder anzuzeigen, die über dem angegebenen Maximum liegen, können Renderer die minimalen und maximalen idealen Größen über die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle nominieren.</span><span class="sxs-lookup"><span data-stu-id="e0fea-115">Although they should still function properly when requested to display images larger than the specified maximum, renderers can nominate the minimum and maximum ideal sizes through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="e0fea-116">Diese Schnittstelle kann nur aufgerufen werden, wenn das Filter Diagramm angehalten oder ausgeführt wird, da es nicht bis zu dem Zeitpunkt ist, zu dem Ressourcen zugewiesen werden, und der Renderer seine Einschränkungen erkennen kann.</span><span class="sxs-lookup"><span data-stu-id="e0fea-116">This interface can be called only when the filter graph is paused or running, because it is not until then that resources are allocated and the renderer can recognize its restrictions.</span></span> <span data-ttu-id="e0fea-117">Wenn keine Einschränkungen vorhanden sind, füllt der Renderer die *pWidth* -und *pHeight* -Parameter mit den nativen Video Dimensionen aus und gibt den Wert \_ false zurück.</span><span class="sxs-lookup"><span data-stu-id="e0fea-117">If no restrictions exist, the renderer fills in the *pWidth* and *pHeight* parameters with the native video dimensions and returns S\_FALSE.</span></span> <span data-ttu-id="e0fea-118">Wenn Einschränkungen vorhanden sind, werden die eingeschränkte Breite und Höhe eingegeben, und die Member-Funktion gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="e0fea-118">If restrictions do exist, the restricted width and height are entered, and the member function returns S\_OK.</span></span>

<span data-ttu-id="e0fea-119">Die Dimensionen gelten für die Größe des Zielvideos und nicht für die gesamte Fenstergröße.</span><span class="sxs-lookup"><span data-stu-id="e0fea-119">The dimensions apply to the size of the destination video and not to the overall window size.</span></span> <span data-ttu-id="e0fea-120">Wenn Sie also die Größe des festzulegenden Fensters berechnen, berücksichtigen Sie die aktuellen Fenster Stile (z \_ . b. WS-Beschriftung und WS-Rahmen \_ ).</span><span class="sxs-lookup"><span data-stu-id="e0fea-120">So, when calculating the size of the window to set, account for the current window styles (for example, WS\_CAPTION and WS\_BORDER).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0fea-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0fea-121">Requirements</span></span>



| <span data-ttu-id="e0fea-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0fea-122">Requirement</span></span> | <span data-ttu-id="e0fea-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e0fea-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0fea-124">Header</span><span class="sxs-lookup"><span data-stu-id="e0fea-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e0fea-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0fea-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0fea-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0fea-126">Library</span></span><br/> | <dl> <span data-ttu-id="e0fea-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e0fea-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0fea-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0fea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0fea-129">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e0fea-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




