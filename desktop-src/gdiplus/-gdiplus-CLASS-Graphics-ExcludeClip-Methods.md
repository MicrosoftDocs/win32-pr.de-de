---
description: In diesem Thema werden die ExcludeClip-Methoden der Grafikklasse aufgeführt. Eine umfassende Liste der Methoden für die Grafikklasse finden Sie unter Grafiken.
ms.assetid: ee2b1bc7-6623-4144-b8fb-2ab9fbe28f59
title: Graphics. ExcludeClip-Methode (gdipl". h")
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 70011bfe1aba7ef8e7c14b58f61bfcbd9549c8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996467"
---
# <a name="graphicsexcludeclip-methods"></a><span data-ttu-id="7b004-104">Graphics. ExcludeClip-Methoden</span><span class="sxs-lookup"><span data-stu-id="7b004-104">Graphics.ExcludeClip methods</span></span>

<span data-ttu-id="7b004-105">In diesem Thema werden die ExcludeClip-Methoden der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b004-105">This topic lists the ExcludeClip methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="7b004-106">Eine umfassende Liste der Methoden für die **Grafik** Klasse finden Sie unter [**Grafiken**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span><span class="sxs-lookup"><span data-stu-id="7b004-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="7b004-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="7b004-107">Overload list</span></span>



| <span data-ttu-id="7b004-108">Methode</span><span class="sxs-lookup"><span data-stu-id="7b004-108">Method</span></span>                                                                         | <span data-ttu-id="7b004-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b004-109">Description</span></span>                                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b004-110">[**Excluentclip (Rect&)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="7b004-110">[**ExcludeClip(Rect&)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))</span></span>   | <span data-ttu-id="7b004-111">Die [**Graphics:: ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_)) -Methode aktualisiert den Clippingbereich auf den Teil von sich selbst, der nicht das angegebene Rechteck überschneidet.</span><span class="sxs-lookup"><span data-stu-id="7b004-111">The [**Graphics::ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_)) method updates the clipping region to the portion of itself that does not intersect the specified rectangle.</span></span><br/>  |
| <span data-ttu-id="7b004-112">[**Excluentclip (RectF&)**](/previous-versions//ms535975(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7b004-112">[**ExcludeClip(RectF&)**](/previous-versions//ms535975(v=vs.85))</span></span> | <span data-ttu-id="7b004-113">Die [**Graphics:: ExcludeClip**](/previous-versions//ms535975(v=vs.85)) -Methode aktualisiert den Clippingbereich auf den Teil von sich selbst, der nicht das angegebene Rechteck überschneidet.</span><span class="sxs-lookup"><span data-stu-id="7b004-113">The [**Graphics::ExcludeClip**](/previous-versions//ms535975(v=vs.85)) method updates the clipping region to the portion of itself that does not intersect the specified rectangle.</span></span><br/> |
| <span data-ttu-id="7b004-114">[**Excludebug (Region \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))</span><span class="sxs-lookup"><span data-stu-id="7b004-114">[**ExcludeClip(Region\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))</span></span>   | <span data-ttu-id="7b004-115">Die [**Graphics:: ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion)) -Methode aktualisiert den Clippingbereich mit dem Teil von sich selbst, der sich nicht mit dem angegebenen Bereich überschneidet.</span><span class="sxs-lookup"><span data-stu-id="7b004-115">The [**Graphics::ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion)) method updates the clipping region with the portion of itself that does not overlap the specified region.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="7b004-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7b004-116">Requirements</span></span>



| <span data-ttu-id="7b004-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b004-117">Requirement</span></span> | <span data-ttu-id="7b004-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7b004-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b004-119">Header</span><span class="sxs-lookup"><span data-stu-id="7b004-119">Header</span></span><br/> | <dl> <span data-ttu-id="7b004-120"><dt>Gdipl-Grafik. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b004-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 
