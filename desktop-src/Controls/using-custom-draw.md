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
# <a name="using-custom-draw"></a>Verwenden benutzerdefinierter zeichnen

Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie benutzerdefiniertes Zeichnen implementiert wird.

Das folgende Code Fragment ist ein Teil eines [**WM- \_ Benachrichtigungs**](wm-notify.md) Handlers, der veranschaulicht, wie benutzerdefinierte Draw-Benachrichtigungen behandelt werden, die an ein Listenansicht-Steuerelement gesendet werden.


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



In der ersten [nm- \_ customdraw](nm-customdraw.md) -Benachrichtigung ist der **dwdrawstage** -Member der [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur auf **CDDs \_ PrePaint** festgelegt. Der Handler gibt [**cdrf \_ notifyitemdraw**](cdrf-constants.md) zurück, um anzugeben, dass er ein oder mehrere Elemente einzeln ändern möchte.

Wenn [**cdrf \_ notifyitemdraw**](cdrf-constants.md) im vorherigen Schritt zurückgegeben wurde, wurde für die nächste [nm- \_ customdraw](nm-customdraw.md) -Benachrichtigung **dwdrawstage** auf **CDDs \_ itemprepaint** festgelegt. Der Handler Ruft die aktuellen Farb-und Schriftart Werte ab. An diesem Punkt können Sie neue Werte für die Modi "Small Icon", "Large Icon" und "List" angeben. Wenn sich das Steuerelement im Berichtsmodus befindet, können Sie auch neue Werte angeben, die auf alle unter Elemente des Elements angewendet werden. Wenn Sie etwas geändert haben, geben Sie [**cdrf \_ newFont**](cdrf-constants.md)zurück. Wenn sich das Steuerelement im Berichtsmodus befindet und Sie die unter Elemente einzeln verarbeiten möchten, geben Sie **cdrf \_ notifysubitemdraw** zurück.

Die letzte Benachrichtigung wird nur gesendet, wenn sich das Steuerelement im Berichtsmodus befindet und Sie **cdrf \_ notifysubitemdraw** im vorherigen Schritt zurückgegeben haben. Das Verfahren zum Ändern von Schriftarten und Farben ist mit diesem Schritt identisch, aber es gilt nur für ein einzelnes Unterelement. Gibt [**cdrf \_ newFont**](cdrf-constants.md) zurück, um das Steuerelement zu benachrichtigen, wenn die Farbe oder Schriftart geändert wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Informationen zum benutzerdefinierten Zeichnen](about-custom-draw.md)
</dt> <dt>

[Benutzerdefinierter Zeichnungs Verweis](custom-draw-reference.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Beispiel: custdtv veranschaulicht benutzerdefiniertes Zeichnen in einer TreeView (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




