---
title: Bild Lauf Leiste (MSAA UI Element Reference)
description: Mithilfe von Bild Lauf leisten können Benutzer die Richtung und die Entfernung auswählen, um einen Bildlauf durch die Informationen in einem verwandten Fenster oder Listenfeld durchführen Der Fenster Klassenname für eine Schiebe Leiste lautet \ 0034; ScrollBar \ 0034;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039551"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a><span data-ttu-id="0ed11-104">Bild Lauf Leiste (MSAA UI Element Reference)</span><span class="sxs-lookup"><span data-stu-id="0ed11-104">Scroll Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="0ed11-105">In diesem Thema werden **ScrollBar** -Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0ed11-105">This topic describes **Scroll Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="0ed11-106">Das Erstellen von **ScrollBar** -Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0ed11-106">How to create **Scroll Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="0ed11-107">Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.</span><span class="sxs-lookup"><span data-stu-id="0ed11-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="0ed11-108">Mithilfe von Bild Lauf leisten können Benutzer die Richtung und die Entfernung auswählen, um einen Bildlauf durch die Informationen in einem verwandten Fenster oder Listenfeld durchführen</span><span class="sxs-lookup"><span data-stu-id="0ed11-108">Scroll bars let a user choose the direction and distance to scroll through information in a related window or list box.</span></span> <span data-ttu-id="0ed11-109">Der Fenster Klassenname für eine Schiebe Leiste ist "ScrollBar".</span><span class="sxs-lookup"><span data-stu-id="0ed11-109">The window class name for a scroll bar is "SCROLLBAR".</span></span>

<span data-ttu-id="0ed11-110">Der Inhalt der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften hängt davon ab, ob die Bild Lauf Leiste vertikal oder horizontal ist und ob die folgenden Teile der Bild Lauf Leiste vom Client abgefragt werden:</span><span class="sxs-lookup"><span data-stu-id="0ed11-110">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depends on whether the scroll bar is vertical or horizontal and on which of the following parts of the scroll bar is being queried by the client:</span></span>

-   <span data-ttu-id="0ed11-111">Die Scrollleiste selbst</span><span class="sxs-lookup"><span data-stu-id="0ed11-111">The scroll bar itself</span></span>
-   <span data-ttu-id="0ed11-112">Die obere oder nach-rechts-Taste</span><span class="sxs-lookup"><span data-stu-id="0ed11-112">The top or right arrow button</span></span>
-   <span data-ttu-id="0ed11-113">Schaltfläche "unten" oder "nach links"</span><span class="sxs-lookup"><span data-stu-id="0ed11-113">The bottom or left arrow button</span></span>
-   <span data-ttu-id="0ed11-114">Das Bild Lauf Feld (Thumb)</span><span class="sxs-lookup"><span data-stu-id="0ed11-114">The scroll box (thumb)</span></span>
-   <span data-ttu-id="0ed11-115">Der Bild-auf-oder Seiten rechten Bereich</span><span class="sxs-lookup"><span data-stu-id="0ed11-115">The page up or page right region</span></span>
-   <span data-ttu-id="0ed11-116">Die Bild-ab-oder linke Seite</span><span class="sxs-lookup"><span data-stu-id="0ed11-116">The page down or page left region</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="0ed11-117">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="0ed11-117">IAccessible Methods</span></span>

<span data-ttu-id="0ed11-118">Eine Schiebe Leiste unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="0ed11-118">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   <span data-ttu-id="0ed11-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)– das Bild Lauf leisten Objekt selbst und der Bild Lauf Zieh Punkt unterstützen die Methode " **accDoDefaultAction** " nicht.</span><span class="sxs-lookup"><span data-stu-id="0ed11-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)—The scroll bar object itself and the scroll thumb do not support the **accDoDefaultAction** method.</span></span>

    <span data-ttu-id="0ed11-120">Für die anderen Bild Lauf leisten Teile auf einer vertikalen Bild Lauf Leiste ruft " [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) " [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) mit der " [**WM \_ VScroll**](/windows/desktop/Controls/wm-vscroll) "-Meldung auf, wobei *wParam* auf die folgenden Werte festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0ed11-120">For the other scroll bar parts on a vertical scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="0ed11-121">Schaltfläche/Region</span><span class="sxs-lookup"><span data-stu-id="0ed11-121">Button/Region</span></span>       | <span data-ttu-id="0ed11-122">Erwarteter</span><span class="sxs-lookup"><span data-stu-id="0ed11-122">Vaule</span></span>        |
    |---------------------|--------------|
    | <span data-ttu-id="0ed11-123">Schaltfläche "Oberer Pfeil</span><span class="sxs-lookup"><span data-stu-id="0ed11-123">Top arrow button</span></span>    | <span data-ttu-id="0ed11-124">SB \_ -Auflistung</span><span class="sxs-lookup"><span data-stu-id="0ed11-124">SB\_LINEUP</span></span>   |
    | <span data-ttu-id="0ed11-125">Schaltfläche zum unteren Pfeil</span><span class="sxs-lookup"><span data-stu-id="0ed11-125">Bottom arrow button</span></span> | <span data-ttu-id="0ed11-126">SB- \_ LineDown</span><span class="sxs-lookup"><span data-stu-id="0ed11-126">SB\_LINEDOWN</span></span> |
    | <span data-ttu-id="0ed11-127">Bild-auf-Seite</span><span class="sxs-lookup"><span data-stu-id="0ed11-127">Page up region</span></span>      | <span data-ttu-id="0ed11-128">SB- \_ PageUp</span><span class="sxs-lookup"><span data-stu-id="0ed11-128">SB\_PAGEUP</span></span>   |
    | <span data-ttu-id="0ed11-129">Bild-ab-Region</span><span class="sxs-lookup"><span data-stu-id="0ed11-129">Page down region</span></span>    | <span data-ttu-id="0ed11-130">SB- \_ PageDown</span><span class="sxs-lookup"><span data-stu-id="0ed11-130">SB\_PAGEDOWN</span></span> |

    

     

    <span data-ttu-id="0ed11-131">Für die anderen Bild Lauf leisten Teile auf einer horizontalen Schiebe Leiste ruft [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) mit der [**WM- \_ HScroll**](/windows/desktop/Controls/wm-hscroll) -Nachricht auf, wobei *wParam* auf die folgenden Werte festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0ed11-131">For the other scroll bar parts on a horizontal scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_HSCROLL**](/windows/desktop/Controls/wm-hscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="0ed11-132">Schaltfläche/Region</span><span class="sxs-lookup"><span data-stu-id="0ed11-132">Button/Region</span></span>      | <span data-ttu-id="0ed11-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0ed11-133">Value</span></span>         |
    |--------------------|---------------|
    | <span data-ttu-id="0ed11-134">Schaltfläche nach links</span><span class="sxs-lookup"><span data-stu-id="0ed11-134">Left arrow button</span></span>  | <span data-ttu-id="0ed11-135">SB- \_ LineLeft</span><span class="sxs-lookup"><span data-stu-id="0ed11-135">SB\_LINELEFT</span></span>  |
    | <span data-ttu-id="0ed11-136">Schaltfläche mit Pfeil nach rechts</span><span class="sxs-lookup"><span data-stu-id="0ed11-136">Right arrow button</span></span> | <span data-ttu-id="0ed11-137">SB- \_ LineRight</span><span class="sxs-lookup"><span data-stu-id="0ed11-137">SB\_LINERIGHT</span></span> |
    | <span data-ttu-id="0ed11-138">Seiten Linker Bereich</span><span class="sxs-lookup"><span data-stu-id="0ed11-138">Page left region</span></span>   | <span data-ttu-id="0ed11-139">SB- \_ PageLeft</span><span class="sxs-lookup"><span data-stu-id="0ed11-139">SB\_PAGELEFT</span></span>  |
    | <span data-ttu-id="0ed11-140">Seite Rechter Bereich</span><span class="sxs-lookup"><span data-stu-id="0ed11-140">Page right region</span></span>  | <span data-ttu-id="0ed11-141">SB- \_ PageRight</span><span class="sxs-lookup"><span data-stu-id="0ed11-141">SB\_PAGERIGHT</span></span> |

    

     

-   [<span data-ttu-id="0ed11-142">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="0ed11-142">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="0ed11-143">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="0ed11-143">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="0ed11-144">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="0ed11-144">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="0ed11-145">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ed11-145">IAccessible Properties</span></span>

<span data-ttu-id="0ed11-146">Eine Schiebe Leiste unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0ed11-146">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="0ed11-147">[**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)– die **childCount** -Eigenschaft für das ScrollBar-Objekt ist 5.</span><span class="sxs-lookup"><span data-stu-id="0ed11-147">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property for the scroll bar object is five.</span></span> <span data-ttu-id="0ed11-148">Für die anderen Bild Lauf leisten Teile ist die **childCount** -Eigenschaft gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0ed11-148">For the other scroll bar parts, the **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="0ed11-149">[**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)– das ScrollBar-Objekt selbst und der Bild Lauf Zieh Punkt unterstützen die **DEFAULTACTION** -Eigenschaft nicht.</span><span class="sxs-lookup"><span data-stu-id="0ed11-149">[**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)—The scroll bar object itself and the scroll thumb do not support the **DefaultAction** property.</span></span> <span data-ttu-id="0ed11-150">Die **DEFAULTACTION** -Eigenschaft für die Pfeil Schaltflächen und die schattierten Bereiche auf beiden Seiten des Bild Lauf Zieh Punkts sind "drücken".</span><span class="sxs-lookup"><span data-stu-id="0ed11-150">The **DefaultAction** property for the arrow buttons and the shaded areas on either side of the scroll thumb is "Press".</span></span>
-   <span data-ttu-id="0ed11-151">[**get \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)– die **Description** -Eigenschaft hängt von dem Teil der Scrollleiste ab, der abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="0ed11-151">[**get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)—The **Description** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="0ed11-152">Die Teile einer vertikalen Schiebe Leiste enthalten die folgenden Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="0ed11-152">The parts of a vertical scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="0ed11-153">Teil</span><span class="sxs-lookup"><span data-stu-id="0ed11-153">Part</span></span>                | <span data-ttu-id="0ed11-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ed11-154">Description</span></span>                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | <span data-ttu-id="0ed11-155">Scrollleiste selbst</span><span class="sxs-lookup"><span data-stu-id="0ed11-155">Scroll bar itself</span></span>   | <span data-ttu-id="0ed11-156">"Wird verwendet, um den vertikalen Anzeigebereich zu ändern."</span><span class="sxs-lookup"><span data-stu-id="0ed11-156">"Used to change the vertical viewing area"</span></span>                                          |
    | <span data-ttu-id="0ed11-157">Schaltfläche "Oberer Pfeil</span><span class="sxs-lookup"><span data-stu-id="0ed11-157">Top arrow button</span></span>    | <span data-ttu-id="0ed11-158">"Verschiebt die vertikale Position um eine Zeile nach oben"</span><span class="sxs-lookup"><span data-stu-id="0ed11-158">"Moves the vertical position up one line"</span></span>                                           |
    | <span data-ttu-id="0ed11-159">Schaltfläche zum unteren Pfeil</span><span class="sxs-lookup"><span data-stu-id="0ed11-159">Bottom arrow button</span></span> | <span data-ttu-id="0ed11-160">"Verschiebt die vertikale Position um eine Zeile nach unten"</span><span class="sxs-lookup"><span data-stu-id="0ed11-160">"Moves the vertical position down one line"</span></span>                                         |
    | <span data-ttu-id="0ed11-161">Bild Lauf Thumb</span><span class="sxs-lookup"><span data-stu-id="0ed11-161">Scroll thumb</span></span>        | <span data-ttu-id="0ed11-162">"Gibt die aktuelle vertikale Position an und kann gezogen werden, um Sie direkt zu ändern."</span><span class="sxs-lookup"><span data-stu-id="0ed11-162">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="0ed11-163">Bild-auf-Seite</span><span class="sxs-lookup"><span data-stu-id="0ed11-163">Page up region</span></span>      | <span data-ttu-id="0ed11-164">"Verschiebt die vertikale Position um einige Zeilen nach oben"</span><span class="sxs-lookup"><span data-stu-id="0ed11-164">"Moves the vertical position up a couple of lines"</span></span>                                  |
    | <span data-ttu-id="0ed11-165">Bild-ab-Region</span><span class="sxs-lookup"><span data-stu-id="0ed11-165">Page down region</span></span>    | <span data-ttu-id="0ed11-166">"Gibt die aktuelle vertikale Position an und kann gezogen werden, um Sie direkt zu ändern."</span><span class="sxs-lookup"><span data-stu-id="0ed11-166">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |

    

     

    <span data-ttu-id="0ed11-167">Die Teile einer horizontalen Schiebe Leiste haben folgende Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="0ed11-167">The parts of a horizontal scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="0ed11-168">Teil</span><span class="sxs-lookup"><span data-stu-id="0ed11-168">Part</span></span>               | <span data-ttu-id="0ed11-169">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ed11-169">Description</span></span>                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="0ed11-170">Scrollleiste selbst</span><span class="sxs-lookup"><span data-stu-id="0ed11-170">Scroll bar itself</span></span>  | <span data-ttu-id="0ed11-171">"Wird verwendet, um den horizontalen Anzeigebereich zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0ed11-171">"Used to change the horizontal viewing area"</span></span>                                          |
    | <span data-ttu-id="0ed11-172">Schaltfläche nach links</span><span class="sxs-lookup"><span data-stu-id="0ed11-172">Left arrow button</span></span>  | <span data-ttu-id="0ed11-173">"Verschiebt die horizontale Position um eine Spalte nach links"</span><span class="sxs-lookup"><span data-stu-id="0ed11-173">"Moves the horizontal position left one column"</span></span>                                       |
    | <span data-ttu-id="0ed11-174">Schaltfläche mit Pfeil nach rechts</span><span class="sxs-lookup"><span data-stu-id="0ed11-174">Right arrow button</span></span> | <span data-ttu-id="0ed11-175">' Verschiebt die horizontale Position um eine Spalte nach rechts</span><span class="sxs-lookup"><span data-stu-id="0ed11-175">'Moves the horizontal position right one column"</span></span>                                      |
    | <span data-ttu-id="0ed11-176">Bild Lauf Thumb</span><span class="sxs-lookup"><span data-stu-id="0ed11-176">Scroll thumb</span></span>       | <span data-ttu-id="0ed11-177">"Gibt die aktuelle horizontale Position an und kann gezogen werden, um Sie direkt zu ändern."</span><span class="sxs-lookup"><span data-stu-id="0ed11-177">"Indicates the current horizontal position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="0ed11-178">Seiten Linker Bereich</span><span class="sxs-lookup"><span data-stu-id="0ed11-178">Page left region</span></span>   | <span data-ttu-id="0ed11-179">"Verschiebt die horizontale Position um eine Reihe von Spalten nach links"</span><span class="sxs-lookup"><span data-stu-id="0ed11-179">"Moves the horizontal position left a couple of columns"</span></span>                              |
    | <span data-ttu-id="0ed11-180">Seite Rechter Bereich</span><span class="sxs-lookup"><span data-stu-id="0ed11-180">Page right region</span></span>  | <span data-ttu-id="0ed11-181">"Gibt die aktuelle vertikale Position an und kann gezogen werden, um Sie direkt zu ändern."</span><span class="sxs-lookup"><span data-stu-id="0ed11-181">"Indicates the current vertical position, and can be dragged to change it directly"</span></span>   |

    

     

-   [<span data-ttu-id="0ed11-182">**\_accHelp erhalten**</span><span class="sxs-lookup"><span data-stu-id="0ed11-182">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="0ed11-183">**\_accHelpTopic erhalten**</span><span class="sxs-lookup"><span data-stu-id="0ed11-183">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="0ed11-184">[**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)– die **Name** -Eigenschaft hängt von dem Teil der Scrollleiste ab, der abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="0ed11-184">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="0ed11-185">Die Teile einer vertikalen Scrollleiste haben die folgenden Namen.</span><span class="sxs-lookup"><span data-stu-id="0ed11-185">The parts of a vertical scroll bar have the following names.</span></span>

    | <span data-ttu-id="0ed11-186">Teil</span><span class="sxs-lookup"><span data-stu-id="0ed11-186">Part</span></span>                | <span data-ttu-id="0ed11-187">Name</span><span class="sxs-lookup"><span data-stu-id="0ed11-187">Name</span></span>        |
    |---------------------|-------------|
    | <span data-ttu-id="0ed11-188">ScrollBar-Fenster</span><span class="sxs-lookup"><span data-stu-id="0ed11-188">Scroll bar window</span></span>   | <span data-ttu-id="0ed11-189">Rechtes</span><span class="sxs-lookup"><span data-stu-id="0ed11-189">"Vertical"</span></span>  |
    | <span data-ttu-id="0ed11-190">Schaltfläche "Oberer Pfeil</span><span class="sxs-lookup"><span data-stu-id="0ed11-190">Top arrow button</span></span>    | <span data-ttu-id="0ed11-191">"Zeile nach oben"</span><span class="sxs-lookup"><span data-stu-id="0ed11-191">"Line up"</span></span>   |
    | <span data-ttu-id="0ed11-192">Schaltfläche zum unteren Pfeil</span><span class="sxs-lookup"><span data-stu-id="0ed11-192">Bottom arrow button</span></span> | <span data-ttu-id="0ed11-193">"Zeile nach unten"</span><span class="sxs-lookup"><span data-stu-id="0ed11-193">"Line down"</span></span> |
    | <span data-ttu-id="0ed11-194">Bild Lauf Thumb</span><span class="sxs-lookup"><span data-stu-id="0ed11-194">Scroll thumb</span></span>        | <span data-ttu-id="0ed11-195">Gebracht</span><span class="sxs-lookup"><span data-stu-id="0ed11-195">"Position"</span></span>  |
    | <span data-ttu-id="0ed11-196">Bild-auf-Seite</span><span class="sxs-lookup"><span data-stu-id="0ed11-196">Page up region</span></span>      | <span data-ttu-id="0ed11-197">"Seite nach oben"</span><span class="sxs-lookup"><span data-stu-id="0ed11-197">"Page up"</span></span>   |
    | <span data-ttu-id="0ed11-198">Bild-ab-Region</span><span class="sxs-lookup"><span data-stu-id="0ed11-198">Page down region</span></span>    | <span data-ttu-id="0ed11-199">"Bild-ab"</span><span class="sxs-lookup"><span data-stu-id="0ed11-199">"Page down"</span></span> |

    

     

    <span data-ttu-id="0ed11-200">Die Teile einer horizontalen Scrollleiste haben die folgenden Namen.</span><span class="sxs-lookup"><span data-stu-id="0ed11-200">The parts of a horizontal scroll bar have the following names.</span></span>

    

    | <span data-ttu-id="0ed11-201">Teil</span><span class="sxs-lookup"><span data-stu-id="0ed11-201">Part</span></span>               | <span data-ttu-id="0ed11-202">Name</span><span class="sxs-lookup"><span data-stu-id="0ed11-202">Name</span></span>           |
    |--------------------|----------------|
    | <span data-ttu-id="0ed11-203">ScrollBar-Fenster</span><span class="sxs-lookup"><span data-stu-id="0ed11-203">Scroll bar window</span></span>  | <span data-ttu-id="0ed11-204">Ales</span><span class="sxs-lookup"><span data-stu-id="0ed11-204">"Horizontal"</span></span>   |
    | <span data-ttu-id="0ed11-205">Schaltfläche nach links</span><span class="sxs-lookup"><span data-stu-id="0ed11-205">Left arrow button</span></span>  | <span data-ttu-id="0ed11-206">"Spalte links"</span><span class="sxs-lookup"><span data-stu-id="0ed11-206">"Column left"</span></span>  |
    | <span data-ttu-id="0ed11-207">Schaltfläche mit Pfeil nach rechts</span><span class="sxs-lookup"><span data-stu-id="0ed11-207">Right arrow button</span></span> | <span data-ttu-id="0ed11-208">"Column right"</span><span class="sxs-lookup"><span data-stu-id="0ed11-208">"Column right"</span></span> |
    | <span data-ttu-id="0ed11-209">Bild Lauf Thumb</span><span class="sxs-lookup"><span data-stu-id="0ed11-209">Scroll thumb</span></span>       | <span data-ttu-id="0ed11-210">Gebracht</span><span class="sxs-lookup"><span data-stu-id="0ed11-210">"Position"</span></span>     |
    | <span data-ttu-id="0ed11-211">Seite Rechter Bereich</span><span class="sxs-lookup"><span data-stu-id="0ed11-211">Page right region</span></span>  | <span data-ttu-id="0ed11-212">"Page Right"</span><span class="sxs-lookup"><span data-stu-id="0ed11-212">"Page right"</span></span>   |
    | <span data-ttu-id="0ed11-213">Seiten Linker Bereich</span><span class="sxs-lookup"><span data-stu-id="0ed11-213">Page left region</span></span>   | <span data-ttu-id="0ed11-214">"Seite Links"</span><span class="sxs-lookup"><span data-stu-id="0ed11-214">"Page left"</span></span>    |

    

     

-   <span data-ttu-id="0ed11-215">[**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)– die **Parent** -Eigenschaft der Pfeil Schaltflächen, der Bild Lauf Zieh Punkt und der schattierte Bereich auf beiden Seiten des Zieh Punkts ist das Fenster der Schiebe Leiste.</span><span class="sxs-lookup"><span data-stu-id="0ed11-215">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the scroll bar window.</span></span> <span data-ttu-id="0ed11-216">Die **Parent** -Eigenschaft des ScrollBar-Fensters ist ein Fenster (Rollen \_ System \_ Fenster), das das Steuerelement umgibt und die **Name** -Eigenschaft und den Fenster Klassennamen aufweist.</span><span class="sxs-lookup"><span data-stu-id="0ed11-216">The **Parent** property of the scroll bar window is a window (ROLE\_SYSTEM\_WINDOW) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="0ed11-217">[**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)– die **Role** -Eigenschaft hängt von dem Teil der Scrollleiste ab, der abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="0ed11-217">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the scroll bar that is queried.</span></span> <span data-ttu-id="0ed11-218">Die Teile einer Scrollleiste haben die folgenden Rollen.</span><span class="sxs-lookup"><span data-stu-id="0ed11-218">The parts of a scroll bar have the following roles.</span></span> 

    | <span data-ttu-id="0ed11-219">Teil</span><span class="sxs-lookup"><span data-stu-id="0ed11-219">Part</span></span>                                                  | <span data-ttu-id="0ed11-220">Role</span><span class="sxs-lookup"><span data-stu-id="0ed11-220">Role</span></span>                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="0ed11-221">Scrollleiste selbst</span><span class="sxs-lookup"><span data-stu-id="0ed11-221">Scroll bar itself</span></span>                                     | [<span data-ttu-id="0ed11-222">**Rollen \_ System- \_ Scrollleiste**</span><span class="sxs-lookup"><span data-stu-id="0ed11-222">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="0ed11-223">Schaltflächen oben, nach unten, Links und nach rechts</span><span class="sxs-lookup"><span data-stu-id="0ed11-223">Top, down, left, and right arrow buttons</span></span>              | [<span data-ttu-id="0ed11-224">**\_ \_ Schaltfläche "Rollen System"**</span><span class="sxs-lookup"><span data-stu-id="0ed11-224">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |
    | <span data-ttu-id="0ed11-225">Bild Lauf Thumb</span><span class="sxs-lookup"><span data-stu-id="0ed11-225">Scroll thumb</span></span>                                          | [<span data-ttu-id="0ed11-226">**Rollen \_ System \_ Indikator**</span><span class="sxs-lookup"><span data-stu-id="0ed11-226">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="0ed11-227">Bild-auf, Bild-ab, Seite Links und Seiten Rechte</span><span class="sxs-lookup"><span data-stu-id="0ed11-227">Page up, page down, page left, and page right regions</span></span> | [<span data-ttu-id="0ed11-228">**\_ \_ Schaltfläche "Rollen System"**</span><span class="sxs-lookup"><span data-stu-id="0ed11-228">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="0ed11-229">[**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)– die **State** -Eigenschaft jeder ScrollBar-Komponente enthält eine Kombination der folgenden [Werte](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0ed11-229">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property of each scroll bar component includes a combination of the following [values](object-state-constants.md).</span></span>

    | <span data-ttu-id="0ed11-230">State</span><span class="sxs-lookup"><span data-stu-id="0ed11-230">State</span></span>                                                                                 | <span data-ttu-id="0ed11-231">Wert</span><span class="sxs-lookup"><span data-stu-id="0ed11-231">Value</span></span>                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="0ed11-232">**Zustands \_ System \_ unsichtbar**</span><span class="sxs-lookup"><span data-stu-id="0ed11-232">**STATE\_SYSTEM\_INVISIBLE**</span></span>](object-state-constants.md)     | <span data-ttu-id="0ed11-233">In der Bild Lauf Leiste selbst gibt dies an, dass die angegebene vertikale oder horizontale Schiebe Leiste nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0ed11-233">For the scroll bar itself, this indicates the specified vertical or horizontal scroll bar does not exist.</span></span> <span data-ttu-id="0ed11-234">Dies bedeutet, dass für die Bild-auf-oder-nach-unten-Bereiche der Ziehpunkt so positioniert ist, dass der Bereich nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0ed11-234">For the page up or page down regions, this indicates the thumb is positioned such that the region does not exist.</span></span> |
    | [<span data-ttu-id="0ed11-235">**Zustands \_ System- \_ Offscreen**</span><span class="sxs-lookup"><span data-stu-id="0ed11-235">**STATE\_SYSTEM\_OFFSCREEN**</span></span>](object-state-constants.md)     | <span data-ttu-id="0ed11-236">In der Bild Lauf Leiste selbst gibt dies an, dass das Fenster so groß ist, dass die angegebene vertikale oder horizontale Schiebe Leiste momentan nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0ed11-236">For the scroll bar itself, this indicates the window is sized such that the specified vertical or horizontal scroll bar is not currently displayed.</span></span>                                                                         |
    | [<span data-ttu-id="0ed11-237">**Zustands \_ System wurde \_ gedrückt**</span><span class="sxs-lookup"><span data-stu-id="0ed11-237">**STATE\_SYSTEM\_PRESSED**</span></span>](object-state-constants.md)         | <span data-ttu-id="0ed11-238">Die Pfeil Schaltfläche oder der Seitenbereich wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="0ed11-238">The arrow button or page region is pressed.</span></span>                                                                                                                                                                                 |
    | [<span data-ttu-id="0ed11-239">**Zustands \_ System nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="0ed11-239">**STATE\_SYSTEM\_UNAVAILABLE**</span></span>](object-state-constants.md) | <span data-ttu-id="0ed11-240">Die Komponente ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0ed11-240">The component is disabled.</span></span>                                                                                                                                                                                                  |

    

     

-   <span data-ttu-id="0ed11-241">[**\_ accValue erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)– die Eigenschaft **Wert** für das Fenster Scrollleiste gibt die Position der Scrollleiste an und ist eine Zeichenfolge, die eine ganze Zahl zwischen 0 und 100 enthält.</span><span class="sxs-lookup"><span data-stu-id="0ed11-241">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the scroll bar window indicates the scroll bar position and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ed11-242">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0ed11-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ed11-243">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0ed11-243">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 