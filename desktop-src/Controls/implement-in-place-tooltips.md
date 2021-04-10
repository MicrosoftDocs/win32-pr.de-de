---
title: Implementieren von In-Place Quick Infos
description: Direkte Quick Infos werden zum Anzeigen von Text Zeichenfolgen für Objekte verwendet, die abgeschnitten wurden. Eine Abbildung finden Sie unter Informationen zu QuickInfo-Steuerelementen.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc321ecdd6df151a151e6d21c8419326edb63d38
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039868"
---
# <a name="how-to-implement-in-place-tooltips"></a><span data-ttu-id="703d9-104">Implementieren von In-Place Quick Infos</span><span class="sxs-lookup"><span data-stu-id="703d9-104">How to Implement In-Place Tooltips</span></span>

<span data-ttu-id="703d9-105">Direkte Quick Infos werden zum Anzeigen von Text Zeichenfolgen für Objekte verwendet, die abgeschnitten wurden.</span><span class="sxs-lookup"><span data-stu-id="703d9-105">In-place tooltips are used to display text strings for objects that have been clipped.</span></span> <span data-ttu-id="703d9-106">Eine Abbildung finden Sie unter [Informationen zu](tooltip-controls.md)QuickInfo-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="703d9-106">For an illustration, see [About Tooltip Controls](tooltip-controls.md).</span></span>

<span data-ttu-id="703d9-107">Der Unterschied zwischen normalen und direkten Quick Infos ist die Positionierung.</span><span class="sxs-lookup"><span data-stu-id="703d9-107">The difference between ordinary and in-place tooltips is positioning.</span></span> <span data-ttu-id="703d9-108">Wenn der Mauszeiger auf einen Bereich zeigt, dem eine QuickInfo zugeordnet ist, wird die QuickInfo standardmäßig neben dem Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="703d9-108">By default, when the mouse pointer hovers over a region that has a tooltip associated with it, the tooltip is displayed adjacent to the region.</span></span> <span data-ttu-id="703d9-109">Quick Infos sind jedoch Windows, und Sie können an einer beliebigen Stelle positioniert werden, indem Sie [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="703d9-109">However, tooltips are windows, and they can be positioned anywhere you choose by calling [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="703d9-110">Das Erstellen einer direkten QuickInfo besteht darin, das QuickInfo-Fenster so zu positionieren, dass es die Text Zeichenfolge überlagert.</span><span class="sxs-lookup"><span data-stu-id="703d9-110">Creating an in-place tooltip is a matter of positioning the tooltip window so that it overlays the text string.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="703d9-111">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="703d9-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="703d9-112">Technologien</span><span class="sxs-lookup"><span data-stu-id="703d9-112">Technologies</span></span>

-   [<span data-ttu-id="703d9-113">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="703d9-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="703d9-114">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="703d9-114">Prerequisites</span></span>

-   <span data-ttu-id="703d9-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="703d9-115">C/C++</span></span>
-   <span data-ttu-id="703d9-116">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="703d9-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="703d9-117">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="703d9-117">Instructions</span></span>

### <a name="positioning-an-in-place-tooltip"></a><span data-ttu-id="703d9-118">Positionieren einer In-Place-QuickInfo</span><span class="sxs-lookup"><span data-stu-id="703d9-118">Positioning an In-Place Tooltip</span></span>

<span data-ttu-id="703d9-119">Sie müssen drei Rechtecke nachverfolgen, wenn Sie eine direkte QuickInfo positionieren:</span><span class="sxs-lookup"><span data-stu-id="703d9-119">You need to keep track of three rectangles when positioning an in-place tooltip:</span></span>

1.  <span data-ttu-id="703d9-120">Das Rechteck, das den vollständigen Bezeichnungs Text umgibt.</span><span class="sxs-lookup"><span data-stu-id="703d9-120">The rectangle that surrounds the complete label text.</span></span>
2.  <span data-ttu-id="703d9-121">Das Rechteck, das den QuickInfo-Text umgibt.</span><span class="sxs-lookup"><span data-stu-id="703d9-121">The rectangle that surrounds the tooltip text.</span></span> <span data-ttu-id="703d9-122">Der QuickInfo-Text ist mit dem vollständigen Bezeichnungs Text identisch und weist normalerweise dieselbe Größe und Schriftart auf.</span><span class="sxs-lookup"><span data-stu-id="703d9-122">The tooltip text is identical to the complete label text, and normally is the same size and font.</span></span> <span data-ttu-id="703d9-123">Die zwei Text Rechtecke haben daher normalerweise dieselbe Größe.</span><span class="sxs-lookup"><span data-stu-id="703d9-123">The two text rectangles will thus usually be the same size.</span></span>
3.  <span data-ttu-id="703d9-124">Das QuickInfo-Fenster Rechteck.</span><span class="sxs-lookup"><span data-stu-id="703d9-124">The tooltip window rectangle.</span></span> <span data-ttu-id="703d9-125">Dieses Rechteck ist etwas größer als das QuickInfo-Text Rechteck, das es einschließt.</span><span class="sxs-lookup"><span data-stu-id="703d9-125">This rectangle is somewhat larger than the tooltip text rectangle that it encloses.</span></span>


<span data-ttu-id="703d9-126">Die drei Rechtecke werden schematisch in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="703d9-126">The three rectangles are shown schematically in the following illustration.</span></span> <span data-ttu-id="703d9-127">Der verborgene Teil des Beschriftungs Texts wird durch einen grauen Hintergrund angegeben.</span><span class="sxs-lookup"><span data-stu-id="703d9-127">The hidden portion of the label text is indicated by a gray background.</span></span>

![das Diagramm zeigt eine lange Zeichenfolge, die Hälfte davon einen grauen Hintergrund hat, dann die gleiche Zeichenfolge innerhalb eines größeren QuickInfo-Fenster Rechtecks.](images/inplace.png)

<span data-ttu-id="703d9-129">Um eine direkte QuickInfo zu erstellen, müssen Sie das QuickInfo-Text Rechteck so positionieren, dass es das Bezeichnungs Text Rechteck überlagert.</span><span class="sxs-lookup"><span data-stu-id="703d9-129">To create an in-place tooltip, you must position the tooltip text rectangle so that it overlays the label text rectangle.</span></span> <span data-ttu-id="703d9-130">Die Vorgehensweise zum Ausrichten der beiden Rechtecke ist relativ unkompliziert:</span><span class="sxs-lookup"><span data-stu-id="703d9-130">The procedure for aligning the two rectangles is relatively straightforward:</span></span>

1.  <span data-ttu-id="703d9-131">Definieren des Bezeichnungs Text Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="703d9-131">Define the label text rectangle.</span></span>
2.  <span data-ttu-id="703d9-132">Positionieren Sie das QuickInfo-Fenster, sodass das Text Rechteck der QuickInfo das Bezeichnungs Text Rechteck überlagert.</span><span class="sxs-lookup"><span data-stu-id="703d9-132">Position the tooltip window so that the tooltip text rectangle overlays the label text rectangle.</span></span>


<span data-ttu-id="703d9-133">In der Praxis ist es in der Regel ausreichend, die obere linke Ecke der beiden Text Rechtecke auszurichten.</span><span class="sxs-lookup"><span data-stu-id="703d9-133">In practice, it is usually sufficient to align the upper-left corner of the two text rectangles.</span></span> <span data-ttu-id="703d9-134">Wenn Sie versuchen, die Größe des QuickInfo-Text Rechtecks exakt mit dem Bezeichnungs Text Rechteck übereinzustimmen, können Probleme mit der QuickInfo angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="703d9-134">Attempting to resize the tooltip text rectangle to exactly match the label text rectangle could cause problems with the tooltip display.</span></span>

<span data-ttu-id="703d9-135">Das Problem mit diesem einfachen Schema besteht darin, dass Sie das QuickInfo-Text Rechteck nicht direkt positionieren können.</span><span class="sxs-lookup"><span data-stu-id="703d9-135">The problem with this simple scheme is that you cannot position the tooltip text rectangle directly.</span></span> <span data-ttu-id="703d9-136">Stattdessen müssen Sie das QuickInfo-Fenster Rechteck direkt oberhalb und Links vom Bezeichnungs Text Rechteck positionieren, damit die Ecken der zwei Text Rechtecke übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="703d9-136">Instead, you must position the tooltip window rectangle just far enough above and to the left of the label text rectangle so that the corners of the two text rectangles coincide.</span></span> <span data-ttu-id="703d9-137">Anders ausgedrückt: Sie müssen den Offset zwischen dem QuickInfo-Fenster Rechteck und dem eingeschlossenen Text Rechteck kennen.</span><span class="sxs-lookup"><span data-stu-id="703d9-137">In other words, you need to know the offset between the tooltip window rectangle and its enclosed text rectangle.</span></span> <span data-ttu-id="703d9-138">Im Allgemeinen gibt es keine einfache Methode zum Ermitteln dieses Offsets.</span><span class="sxs-lookup"><span data-stu-id="703d9-138">In general, there is no simple way to determine this offset.</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="703d9-139">Implementieren von In-Place Quick Infos</span><span class="sxs-lookup"><span data-stu-id="703d9-139">Implement In-Place Tooltips</span></span>

<span data-ttu-id="703d9-140">Im folgenden Code Fragment wird veranschaulicht, wie eine [**TTM \_**](ttm-adjustrect.md) -Nachricht in einem [TTN- \_ Show](ttn-show.md) Handler verwendet wird, um eine direkte QuickInfo anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="703d9-140">The following code fragment illustrates how to use a [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message in a [TTN\_SHOW](ttn-show.md) handler to display an in-place tooltip.</span></span> <span data-ttu-id="703d9-141">Die Anwendung gibt an, dass der Bezeichnungs Text abgeschnitten wird, indem die private *fmystringistruncated* -Variable auf **true** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="703d9-141">Your application indicates that the label text is truncated by setting the private *fMyStringIsTruncated* variable to **TRUE**.</span></span> <span data-ttu-id="703d9-142">Der Handler Ruft die Anwendungs definierte Funktion **getmyitemrect** auf, um das Bezeichnungs Text Rechteck abzurufen.</span><span class="sxs-lookup"><span data-stu-id="703d9-142">The handler calls an application-defined function, **GetMyItemRect**, to retrieve the label text rectangle.</span></span> <span data-ttu-id="703d9-143">Dieses Rechteck wird an das QuickInfo-Steuerelement mit TTM-"-", "-", das das entsprechende Fenster Rechteck zurückgibt. **\_**</span><span class="sxs-lookup"><span data-stu-id="703d9-143">This rectangle is passed to the tooltip control with **TTM\_ADJUSTRECT**, which returns the corresponding window rectangle.</span></span> <span data-ttu-id="703d9-144">[**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) wird dann aufgerufen, um die QuickInfo über der Bezeichnung zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="703d9-144">[**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) is then called to position the tooltip over the label.</span></span>


```C++
case TTN_SHOW:
            
    if (fMyStringIsTruncated) 
    {
        RECT rc;
        
        GetMyItemRect(&rc);
        
        SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
        
        SetWindowPos(hwndToolTip, NULL, rc.left, rc.top, 0, 0, 
                     SWP_NOSIZE | SWP_NOZORDER | SWP_NOACTIVATE);
    }
```



<span data-ttu-id="703d9-145">In diesem Beispiel wird die Größe der QuickInfo nicht geändert, sondern nur die Position.</span><span class="sxs-lookup"><span data-stu-id="703d9-145">This example does not change the size of the tooltip, just its position.</span></span> <span data-ttu-id="703d9-146">Die zwei Text Rechtecke werden an Ihren oberen linken Ecken ausgerichtet, aber nicht unbedingt mit denselben Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="703d9-146">The two text rectangles are aligned at their upper-left corners, but not necessarily with the same dimensions.</span></span> <span data-ttu-id="703d9-147">In der Praxis ist der Unterschied in der Regel gering, und diese Vorgehensweise wird für die meisten Zwecke empfohlen.</span><span class="sxs-lookup"><span data-stu-id="703d9-147">In practice, the difference is usually small, and this approach is recommended for most purposes.</span></span> <span data-ttu-id="703d9-148">Obwohl Sie [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) zum Ändern der Größe und zum Neupositionieren der QuickInfo verwenden können, kann dies zu unvorhersehbaren Folgen führen.</span><span class="sxs-lookup"><span data-stu-id="703d9-148">While you can, in principle, use [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) to resize as well as reposition the tooltip, doing so might have unpredictable consequences.</span></span>

## <a name="remarks"></a><span data-ttu-id="703d9-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="703d9-149">Remarks</span></span>

<span data-ttu-id="703d9-150">Allgemeine Steuerelemente [Version 5,80](common-control-versions.md) vereinfachen die Verwendung von direkten Quick Infos durch das Hinzufügen einer neuen Nachricht, [**TTM- \_**](ttm-adjustrect.md)Version.</span><span class="sxs-lookup"><span data-stu-id="703d9-150">Common controls [version 5.80](common-control-versions.md) simplifies the use of in-place tooltips by the addition of a new message, [**TTM\_ADJUSTRECT**](ttm-adjustrect.md).</span></span> <span data-ttu-id="703d9-151">Senden Sie diese Nachricht mit den Koordinaten des Beschriftungs Text Rechtecks, das von der QuickInfo überlagern werden soll, und gibt die Koordinaten eines ordnungsgemäß positionierten QuickInfo-Fenster Rechtecks zurück.</span><span class="sxs-lookup"><span data-stu-id="703d9-151">Send this message with the coordinates of the label text rectangle that you want the tooltip to overlay, and it returns the coordinates of an appropriately positioned tooltip window rectangle.</span></span>

## <a name="related-topics"></a><span data-ttu-id="703d9-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="703d9-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="703d9-153">Verwenden von Quick Infos</span><span class="sxs-lookup"><span data-stu-id="703d9-153">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 