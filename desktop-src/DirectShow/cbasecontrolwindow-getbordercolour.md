---
description: Die getBorderColor-Methode ruft die aktuelle Fensterrahmen Farbe (m \_ BorderColor) ab.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Cbasecontrolwindow. getBorderColor-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367083"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a><span data-ttu-id="64987-103">Cbasecontrolwindow. getBorderColor-Methode</span><span class="sxs-lookup"><span data-stu-id="64987-103">CBaseControlWindow.GetBorderColour method</span></span>

<span data-ttu-id="64987-104">Die- `GetBorderColour` Methode ruft die aktuelle Fensterrahmen Farbe ( **m \_ BorderColor**) ab.</span><span class="sxs-lookup"><span data-stu-id="64987-104">The `GetBorderColour` method retrieves the current window border color, **m\_BorderColour**.</span></span>

## <a name="syntax"></a><span data-ttu-id="64987-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64987-105">Syntax</span></span>


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a><span data-ttu-id="64987-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="64987-106">Parameters</span></span>

<span data-ttu-id="64987-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="64987-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64987-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64987-108">Return value</span></span>

<span data-ttu-id="64987-109">Gibt die Farbe des Rahmens zurück.</span><span class="sxs-lookup"><span data-stu-id="64987-109">Returns the color of the border.</span></span>

## <a name="remarks"></a><span data-ttu-id="64987-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64987-110">Remarks</span></span>

<span data-ttu-id="64987-111">Eine Anwendung kann ein Ziel Rechteck festlegen, um das Video anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64987-111">An application can set a destination rectangle to display the video.</span></span> <span data-ttu-id="64987-112">Dieses Rechteck sollte relativ zum Client Bereich des Fensters sein.</span><span class="sxs-lookup"><span data-stu-id="64987-112">This rectangle should be relative to the client area for the window.</span></span> <span data-ttu-id="64987-113">Wenn dies geschieht (Standardmäßig wird das gesamte Fenster gezeichnet), gibt es einen Bereich, in dem das Video umgeben ist. Das heißt, der Rahmen.</span><span class="sxs-lookup"><span data-stu-id="64987-113">If this is done (the default is to always paint the entire window), there is an area that surrounds the video; that is, the border.</span></span> <span data-ttu-id="64987-114">Die Rahmenfarbe kann über die Funktion " [**cbasecontrolwindow::p UT \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) Member" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64987-114">The border color can be set through the [**CBaseControlWindow::put\_BorderColor**](cbasecontrolwindow-put-bordercolor.md) member function.</span></span> <span data-ttu-id="64987-115">Diese Eigenschaft wirkt sich auf die Rahmenfarbe aus.</span><span class="sxs-lookup"><span data-stu-id="64987-115">This property affects the color of the border.</span></span> <span data-ttu-id="64987-116">Verwenden Sie diese Member-Funktion anstelle von [**cbasecontrolwindow:: get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), es sei denn, Sie rufen dies extern über die [**IVideoWindow:: get \_ BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="64987-116">Use this member function instead of [**CBaseControlWindow::get\_BorderColor**](cbasecontrolwindow-get-bordercolor.md), unless you are calling this externally through the [**IVideoWindow::get\_BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="64987-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64987-117">Requirements</span></span>



| <span data-ttu-id="64987-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64987-118">Requirement</span></span> | <span data-ttu-id="64987-119">Wert</span><span class="sxs-lookup"><span data-stu-id="64987-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64987-120">Header</span><span class="sxs-lookup"><span data-stu-id="64987-120">Header</span></span><br/>  | <dl> <span data-ttu-id="64987-121"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64987-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="64987-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="64987-122">Library</span></span><br/> | <dl> <span data-ttu-id="64987-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="64987-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64987-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64987-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64987-125">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="64987-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




