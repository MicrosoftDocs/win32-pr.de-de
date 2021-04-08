---
title: Verwenden benutzerdefinierter zeichnen
description: Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie benutzerdefiniertes Zeichnen implementiert wird.
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0b8a2585103aa27a27f0138a49885cc726d3b1
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038614"
---
# <a name="using-custom-draw"></a><span data-ttu-id="9662c-103">Verwenden benutzerdefinierter zeichnen</span><span class="sxs-lookup"><span data-stu-id="9662c-103">Using Custom Draw</span></span>

<span data-ttu-id="9662c-104">Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie benutzerdefiniertes Zeichnen implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="9662c-104">This section contains examples that demonstrate how to implement custom draw.</span></span>

<span data-ttu-id="9662c-105">Das folgende Code Fragment ist ein Teil eines [**WM- \_ Benachrichtigungs**](wm-notify.md) Handlers, der veranschaulicht, wie benutzerdefinierte Draw-Benachrichtigungen behandelt werden, die an ein Listenansicht-Steuerelement gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9662c-105">The following code fragment is a portion of a [**WM\_NOTIFY**](wm-notify.md) handler that illustrates how to handle custom draw notifications sent to a list-view control.</span></span>


```C++
        
LPNMLISTVIEW  pnm  = (LPNMLISTVIEW)lParam;

switch (pnm->hdr.code){
...
case NM_CUSTOMDRAW:

    LPNMLVCUSTOMDRAW  lplvcd = (LPNMLVCUSTOMDRAW)lParam;

    switch(lplvcd->nmcd.dwDrawStage) {

    case CDDS_PREPAINT :
        return CDRF_NOTIFYITEMDRAW;

    case CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForItem(lplvcd->nmcd.dwItemSpec,
                                    lplvcd->nmcd.lItemlParam) );
        lplvcd->clrText = GetColorForItem(lplvcd->nmcd.dwItemSpec,
                                          lplvcd->nmcd.lItemlParam);
        lplvcd->clrTextBk = GetBkColorForItem(lplvcd->nmcd.dwItemSpec,
                                              lplvcd->nmcd.lItemlParam);

/* At this point, you can change the background colors for the item
and any subitems and return CDRF_NEWFONT. If the list-view control
is in report mode, you can simply return CDRF_NOTIFYSUBITEMDRAW
to customize the item's subitems individually */
        ...

        return CDRF_NEWFONT;
    //  or return CDRF_NOTIFYSUBITEMDRAW;

    case CDDS_SUBITEM | CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForSubItem(lplvcd->nmcd.dwItemSpec,
                                       lplvcd->nmcd.lItemlParam,
                                       lplvcd->iSubItem));
        lplvcd->clrText = GetColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                             lplvcd->nmcd.lItemlParam,
                                             lplvcd->iSubItem));
        lplvcd->clrTextBk = GetBkColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                                 lplvcd->nmcd.lItemlParam,
                                                 lplvcd->iSubItem));

/* This notification is received only if you are in report mode and
returned CDRF_NOTIFYSUBITEMDRAW in the previous step. At
this point, you can change the background colors for the
subitem and return CDRF_NEWFONT.*/
        ...
        return CDRF_NEWFONT;    
    }
...
}
        
```



<span data-ttu-id="9662c-106">In der ersten [nm- \_ customdraw](nm-customdraw.md) -Benachrichtigung ist der **dwdrawstage** -Member der [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur auf **CDDs \_ PrePaint** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9662c-106">The first [NM\_CUSTOMDRAW](nm-customdraw.md) notification has the **dwDrawStage** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure set to **CDDS\_PREPAINT**.</span></span> <span data-ttu-id="9662c-107">Der Handler gibt [**cdrf \_ notifyitemdraw**](cdrf-constants.md) zurück, um anzugeben, dass er ein oder mehrere Elemente einzeln ändern möchte.</span><span class="sxs-lookup"><span data-stu-id="9662c-107">The handler returns [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) to indicate that it wishes to modify one or more items individually.</span></span>

<span data-ttu-id="9662c-108">Wenn [**cdrf \_ notifyitemdraw**](cdrf-constants.md) im vorherigen Schritt zurückgegeben wurde, wurde für die nächste [nm- \_ customdraw](nm-customdraw.md) -Benachrichtigung **dwdrawstage** auf **CDDs \_ itemprepaint** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9662c-108">If [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) was returned in the previous step, the next [NM\_CUSTOMDRAW](nm-customdraw.md) notification has **dwDrawStage** set to **CDDS\_ITEMPREPAINT**.</span></span> <span data-ttu-id="9662c-109">Der Handler Ruft die aktuellen Farb-und Schriftart Werte ab.</span><span class="sxs-lookup"><span data-stu-id="9662c-109">The handler retrieves the current color and font values.</span></span> <span data-ttu-id="9662c-110">An diesem Punkt können Sie neue Werte für die Modi "Small Icon", "Large Icon" und "List" angeben.</span><span class="sxs-lookup"><span data-stu-id="9662c-110">At this point, you can specify new values for small icon, large icon, and list modes.</span></span> <span data-ttu-id="9662c-111">Wenn sich das Steuerelement im Berichtsmodus befindet, können Sie auch neue Werte angeben, die auf alle unter Elemente des Elements angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9662c-111">If the control is in report mode, you can also specify new values that will apply to all subitems of the item.</span></span> <span data-ttu-id="9662c-112">Wenn Sie etwas geändert haben, geben Sie [**cdrf \_ newFont**](cdrf-constants.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="9662c-112">If you have changed anything, return [**CDRF\_NEWFONT**](cdrf-constants.md).</span></span> <span data-ttu-id="9662c-113">Wenn sich das Steuerelement im Berichtsmodus befindet und Sie die unter Elemente einzeln verarbeiten möchten, geben Sie **cdrf \_ notifysubitemdraw** zurück.</span><span class="sxs-lookup"><span data-stu-id="9662c-113">If the control is in report mode and you want to handle the subitems individually, return **CDRF\_NOTIFYSUBITEMDRAW**.</span></span>

<span data-ttu-id="9662c-114">Die letzte Benachrichtigung wird nur gesendet, wenn sich das Steuerelement im Berichtsmodus befindet und Sie **cdrf \_ notifysubitemdraw** im vorherigen Schritt zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="9662c-114">The final notification is only sent if the control is in report mode and you returned **CDRF\_NOTIFYSUBITEMDRAW** in the previous step.</span></span> <span data-ttu-id="9662c-115">Das Verfahren zum Ändern von Schriftarten und Farben ist mit diesem Schritt identisch, aber es gilt nur für ein einzelnes Unterelement.</span><span class="sxs-lookup"><span data-stu-id="9662c-115">The procedure for changing fonts and colors is the same as that step, but it only applies to a single subitem.</span></span> <span data-ttu-id="9662c-116">Gibt [**cdrf \_ newFont**](cdrf-constants.md) zurück, um das Steuerelement zu benachrichtigen, wenn die Farbe oder Schriftart geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="9662c-116">Return [**CDRF\_NEWFONT**](cdrf-constants.md) to notify the control if the color or font was changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9662c-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9662c-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9662c-118">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9662c-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9662c-119">Informationen zum benutzerdefinierten Zeichnen</span><span class="sxs-lookup"><span data-stu-id="9662c-119">About Custom Draw</span></span>](about-custom-draw.md)
</dt> <dt>

[<span data-ttu-id="9662c-120">Benutzerdefinierter Zeichnungs Verweis</span><span class="sxs-lookup"><span data-stu-id="9662c-120">Custom Draw Reference</span></span>](custom-draw-reference.md)
</dt> <dt>

<span data-ttu-id="9662c-121">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="9662c-121">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9662c-122">Beispiel: custdtv veranschaulicht benutzerdefiniertes Zeichnen in einer TreeView (Q248496)</span><span class="sxs-lookup"><span data-stu-id="9662c-122">SAMPLE: CustDTv Illustrates Custom Draw in a TreeView (Q248496)</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




