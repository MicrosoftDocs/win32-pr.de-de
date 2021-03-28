---
description: 'Die Grafikklasse bietet eine Vielzahl von Zeichnungs Methoden, einschließlich der in der folgenden Liste aufgeführten Zeichnungs Methoden:'
ms.assetid: d3c8d16c-858a-42a9-a512-3fcfa144f5fc
title: Verwenden eines Stiftes zum Zeichnen von Linien und Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904f53149038d6109365adddc11d3c37881a8def
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129053"
---
# <a name="using-a-pen-to-draw-lines-and-shapes"></a><span data-ttu-id="f06ec-103">Verwenden eines Stiftes zum Zeichnen von Linien und Formen</span><span class="sxs-lookup"><span data-stu-id="f06ec-103">Using a Pen to Draw Lines and Shapes</span></span>

<span data-ttu-id="f06ec-104">Die [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse bietet eine Vielzahl von Zeichnungs Methoden, einschließlich der in der folgenden Liste aufgeführten Zeichnungs Methoden:</span><span class="sxs-lookup"><span data-stu-id="f06ec-104">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides a variety of drawing methods including those shown in the following list:</span></span>

-   <span data-ttu-id="f06ec-105">[DrawLine-Methoden](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span><span class="sxs-lookup"><span data-stu-id="f06ec-105">[DrawLine Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span></span>
-   <span data-ttu-id="f06ec-106">[Drawrechteck-Methoden](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="f06ec-106">[DrawRectangle Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="f06ec-107">[DrawEllipse-Methoden](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="f06ec-107">[DrawEllipse Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="f06ec-108">[DrawArc-Methoden](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span><span class="sxs-lookup"><span data-stu-id="f06ec-108">[DrawArc Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span></span>
-   [<span data-ttu-id="f06ec-109">**Grafiken::D rawpath**</span><span class="sxs-lookup"><span data-stu-id="f06ec-109">**Graphics::DrawPath**</span></span>](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath)
-   <span data-ttu-id="f06ec-110">[DrawCurve-Methoden](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="f06ec-110">[DrawCurve Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span></span>
-   <span data-ttu-id="f06ec-111">[DrawBezier-Methoden](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span><span class="sxs-lookup"><span data-stu-id="f06ec-111">[DrawBezier Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span></span>

<span data-ttu-id="f06ec-112">Eines der Argumente, das Sie an eine solche Zeichnungs Methode übergeben, ist die Adresse eines [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Objekts.</span><span class="sxs-lookup"><span data-stu-id="f06ec-112">One of the arguments that you pass to such a drawing method is the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span>

<span data-ttu-id="f06ec-113">In den folgenden Themen wird die Verwendung von-Stiften ausführlicher behandelt:</span><span class="sxs-lookup"><span data-stu-id="f06ec-113">The following topics cover the use of pens in more detail:</span></span>

-   [<span data-ttu-id="f06ec-114">Verwenden eines Stifts zum Zeichnen von Linien und Rechtecken</span><span class="sxs-lookup"><span data-stu-id="f06ec-114">Using a Pen to Draw Lines and Rectangles</span></span>](-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use.md)
-   [<span data-ttu-id="f06ec-115">Festlegen der Stift Breite und-Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="f06ec-115">Setting Pen Width and Alignment</span></span>](-gdiplus-setting-pen-width-and-alignment-use.md)
-   [<span data-ttu-id="f06ec-116">Zeichnen einer Linie mit Linien Deckeln</span><span class="sxs-lookup"><span data-stu-id="f06ec-116">Drawing a Line with Line Caps</span></span>](-gdiplus-drawing-a-line-with-line-caps-use.md)
-   [<span data-ttu-id="f06ec-117">Joinlinien</span><span class="sxs-lookup"><span data-stu-id="f06ec-117">Joining Lines</span></span>](-gdiplus-joining-lines-use.md)
-   [<span data-ttu-id="f06ec-118">Zeichnen einer benutzerdefinierten gestrichelten Linie</span><span class="sxs-lookup"><span data-stu-id="f06ec-118">Drawing a Custom Dashed Line</span></span>](-gdiplus-drawing-a-custom-dashed-line-use.md)
-   [<span data-ttu-id="f06ec-119">Zeichnen einer mit einer Textur ausgefüllten Linie</span><span class="sxs-lookup"><span data-stu-id="f06ec-119">Drawing a Line Filled with a Texture</span></span>](-gdiplus-drawing-a-line-filled-with-a-texture-use.md)

 

 



