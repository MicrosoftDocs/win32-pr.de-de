---
title: Verwenden von benutzerdefiniertem Zeichnen
description: Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie benutzerdefiniertes Zeichnen implementiert wird.
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90cff5fd4d692d31b69c85980f872f3aca4504cad81a3439d0c4d31a4c73d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655870"
---
# <a name="using-custom-draw"></a>Verwenden von benutzerdefiniertem Zeichnen

Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie benutzerdefiniertes Zeichnen implementiert wird.

Das folgende Codefragment ist ein Teil eines [**WM NOTIFY-Handlers, \_**](wm-notify.md) der veranschaulicht, wie benutzerdefinierte Zeichnen-Benachrichtigungen behandelt werden, die an ein Listenansicht-Steuerelement gesendet werden.


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



Bei der ersten [NM \_ CUSTOMDRAW-Benachrichtigung](nm-customdraw.md) ist **das dwDrawStage-Member** der [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) auf **CDDS \_ PREPAINT festgelegt.** Der Handler gibt [**CDRF \_ NOTIFYITEMDRAW zurück,**](cdrf-constants.md) um anzugeben, dass ein oder mehrere Elemente einzeln geändert werden sollen.

Wenn [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) im vorherigen Schritt zurückgegeben wurde, ist für die nächste [NM \_ CUSTOMDRAW-Benachrichtigung](nm-customdraw.md) **dwDrawStage** auf **CDDS \_ ITEMPREPAINT festgelegt.** Der Handler ruft die aktuelle Farbe und die aktuellen Schriftartwerte ab. An diesem Punkt können Sie neue Werte für kleine Symbole, große Symbole und Listenmodi angeben. Wenn sich das Steuerelement im Berichtsmodus befindet, können Sie auch neue Werte angeben, die für alle Unteritems des Elements gelten. Wenn Sie etwas geändert haben, geben Sie [**CDRF \_ NEWFONT zurück.**](cdrf-constants.md) Wenn sich das Steuerelement im Berichtsmodus befindet und Sie die Unteritems einzeln behandeln möchten, geben Sie **CDRF \_ NOTIFYSUBITEMDRAW zurück.**

Die endgültige Benachrichtigung wird nur gesendet, wenn sich das Steuerelement im Berichtsmodus befindet und Sie im vorherigen Schritt **CDRF \_ NOTIFYSUBITEMDRAW** zurückgegeben haben. Das Verfahren zum Ändern von Schriftarten und Farben ist mit diesem Schritt identisch, gilt aber nur für ein einzelnes Unterem. Geben [**Sie CDRF \_ NEWFONT zurück,**](cdrf-constants.md) um das Steuerelement zu benachrichtigen, wenn die Farbe oder Schriftart geändert wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Informationen zum benutzerdefinierten Zeichnen](about-custom-draw.md)
</dt> <dt>

[Benutzerdefinierter Draw-Verweis](custom-draw-reference.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[BEISPIEL: CustDTv veranschaulicht benutzerdefiniertes Zeichnen in einer TreeView (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




