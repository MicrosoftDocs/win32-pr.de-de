---
description: Die getdefaultrect-Methode ruft die Standardgröße des Client Bereichs ab.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Cbasewindow. getdefaultrect-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d7ec9612eab45e21262f8344daf7a52a6a888b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370684"
---
# <a name="cbasewindowgetdefaultrect-method"></a><span data-ttu-id="a2d3d-103">Cbasewindow. getdefaultrect-Methode</span><span class="sxs-lookup"><span data-stu-id="a2d3d-103">CBaseWindow.GetDefaultRect method</span></span>

<span data-ttu-id="a2d3d-104">Die- `GetDefaultRect` Methode ruft die Standardgröße des Client Bereichs ab.</span><span class="sxs-lookup"><span data-stu-id="a2d3d-104">The `GetDefaultRect` method retrieves the default size of the client area.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2d3d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2d3d-105">Syntax</span></span>


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a><span data-ttu-id="a2d3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2d3d-106">Parameters</span></span>

<span data-ttu-id="a2d3d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a2d3d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2d3d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2d3d-108">Return value</span></span>

<span data-ttu-id="a2d3d-109">Gibt das Standard Rechteck zurück.</span><span class="sxs-lookup"><span data-stu-id="a2d3d-109">Returns the default rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2d3d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2d3d-110">Remarks</span></span>

<span data-ttu-id="a2d3d-111">Wenn das Fenster aktiviert ist, ruft das-Objekt diese Methode auf, um zu bestimmen, wie groß es den Client Bereich des Fensters machen soll.</span><span class="sxs-lookup"><span data-stu-id="a2d3d-111">When the window is activated, the object calls this method to determine how large it should make the window's client area.</span></span> <span data-ttu-id="a2d3d-112">In der Basisklasse gibt diese Methode ein Rechteck zurück, dessen Höhe und Breite die definierten Konstanten "defheight" und "defwidth" sind.</span><span class="sxs-lookup"><span data-stu-id="a2d3d-112">In the base class, this method returns a rectangle whose height and width are the defined constants DEFHEIGHT and DEFWIDTH.</span></span> <span data-ttu-id="a2d3d-113">Eine abgeleitete Klasse sollte diese Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="a2d3d-113">A derived class should override this method.</span></span> <span data-ttu-id="a2d3d-114">Bei einem Videorenderer gibt die abgeleitete Klasse in der Regel die Größe des systemeigenen Video Bilds zurück.</span><span class="sxs-lookup"><span data-stu-id="a2d3d-114">For a video renderer, the derived class will typically return the size of the native video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2d3d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2d3d-115">Requirements</span></span>



| <span data-ttu-id="a2d3d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2d3d-116">Requirement</span></span> | <span data-ttu-id="a2d3d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a2d3d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d3d-118">Header</span><span class="sxs-lookup"><span data-stu-id="a2d3d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a2d3d-119"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2d3d-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2d3d-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a2d3d-120">Library</span></span><br/> | <dl> <span data-ttu-id="a2d3d-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a2d3d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2d3d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2d3d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d3d-123">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a2d3d-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




