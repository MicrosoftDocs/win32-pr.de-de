---
title: List-View Fensterstile (CommCtrl.h)
description: Die folgenden Fensterstile gelten speziell für Listenansichtssteuerelemente.
ms.assetid: 8b57239b-112e-4fb6-b394-15501bd3f5b3
topic_type:
- apiref
api_name:
- LVS_ALIGNLEFT
- LVS_ALIGNMASK
- LVS_ALIGNTOP
- LVS_AUTOARRANGE
- LVS_EDITLABELS
- LVS_ICON
- LVS_LIST
- LVS_NOCOLUMNHEADER
- LVS_NOLABELWRAP
- LVS_NOSCROLL
- LVS_NOSORTHEADER
- LVS_OWNERDATA
- LVS_OWNERDRAWFIXED
- LVS_REPORT
- LVS_SHAREIMAGELISTS
- LVS_SHOWSELALWAYS
- LVS_SINGLESEL
- LVS_SMALLICON
- LVS_SORTASCENDING
- LVS_SORTDESCENDING
- LVS_TYPEMASK
- LVS_TYPESTYLEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e326f4508d08f1052747e64ea5eba184f45f7e73a1cb55539255a27fd8c8c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412025"
---
# <a name="list-view-window-styles"></a>List-View Fensterstile

Die folgenden Fensterstile gelten speziell für Listenansichtssteuerelemente.



| Konstante                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVS_ALIGNLEFT"></span><span id="lvs_alignleft"></span><dl> <dt>**LVS \_ ALIGNLEFT**</dt> </dl>                   | Elemente werden linksbündig im Symbol und in der kleinen Symbolansicht ausgerichtet. <br/>                                                                                                                                                                                                                                                                                             |
| <span id="LVS_ALIGNMASK"></span><span id="lvs_alignmask"></span><dl> <dt>**LVS \_ ALIGNMASK**</dt> </dl>                   | Die aktuelle Ausrichtung des Steuerelements. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="LVS_ALIGNTOP"></span><span id="lvs_aligntop"></span><dl> <dt>**LVS \_ ALIGNTOP**</dt> </dl>                      | Elemente werden am oberen Ende des Listenansicht-Steuerelements in der Symbol- und kleinen Symbolansicht ausgerichtet. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_AUTOARRANGE"></span><span id="lvs_autoarrange"></span><dl> <dt>**LVS \_ AUTOARRANGE**</dt> </dl>             | Symbole werden automatisch in der Symbol- und kleinen Symbolansicht angeordnet. <br/>                                                                                                                                                                                                                                                                              |
| <span id="LVS_EDITLABELS"></span><span id="lvs_editlabels"></span><dl> <dt>**LVS \_ EDITLABELS**</dt> </dl>                | Elementtext kann vor Ort bearbeitet werden. Das übergeordnete Fenster muss den [LVN \_ ENDLABELEDIT-Benachrichtigungscode](lvn-endlabeledit.md) verarbeiten. <br/>                                                                                                                                                                                                               |
| <span id="LVS_ICON"></span><span id="lvs_icon"></span><dl> <dt>**\_LVS-SYMBOL**</dt> </dl>                                  | Dieser Stil gibt die Symbolansicht an. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_LIST"></span><span id="lvs_list"></span><dl> <dt>**LVS \_ LIST**</dt> </dl>                                  | Dieses Format gibt die Listenansicht an. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_NOCOLUMNHEADER"></span><span id="lvs_nocolumnheader"></span><dl> <dt>**LVS \_ NOCOLUMNHEADER**</dt> </dl>    | Spaltenüberschriften werden in der Berichtsansicht nicht angezeigt. Standardmäßig verfügen Spalten in der Berichtsansicht über Kopfzeilen. <br/>                                                                                                                                                                                                                                               |
| <span id="LVS_NOLABELWRAP"></span><span id="lvs_nolabelwrap"></span><dl> <dt>**LVS \_ NOLABELWRAP**</dt> </dl>             | Der Elementtext wird in einer einzelnen Zeile in der Symbolansicht angezeigt. Standardmäßig kann Elementtext in der Symbolansicht umschließen. <br/>                                                                                                                                                                                                                                              |
| <span id="LVS_NOSCROLL"></span><span id="lvs_noscroll"></span><dl> <dt>**LVS \_ NOSCROLL**</dt> </dl>                      | Das Scrollen ist deaktiviert. Alle Elemente müssen sich innerhalb des Clientbereichs enthalten. Dieser Stil ist nicht mit den **LVS \_ LIST- oder** **LVS \_ REPORT-Formaten** kompatibel. Weitere Informationen Knowledge Base Artikel Q137520 finden Sie im Artikel Q137520. <br/>                                                                                                                                      |
| <span id="LVS_NOSORTHEADER"></span><span id="lvs_nosortheader"></span><dl> <dt>**LVS \_ NOSORTHEADER**</dt> </dl>          | Spaltenüberschriften funktionieren nicht wie Schaltflächen. Dieses Format kann verwendet werden, wenn beim Klicken auf eine Spaltenüberschrift in der Berichtsansicht keine Aktion wie z. B. sortierung durchgeführt wird. <br/>                                                                                                                                                                                       |
| <span id="LVS_OWNERDATA"></span><span id="lvs_ownerdata"></span><dl> <dt>**LVS \_ OWNERDATA**</dt> </dl>                   | [Version 4.70](common-control-versions.md). Dieser Stil gibt ein virtuelles Listenansicht-Steuerelement an. Weitere Informationen zu diesem Listensteuerelementestil finden Sie unter [Informationen zu List-View Steuerelementen.](list-view-controls-overview.md) <br/>                                                                                                                             |
| <span id="LVS_OWNERDRAWFIXED"></span><span id="lvs_ownerdrawfixed"></span><dl> <dt>**LVS \_ OWNERDRAWFIXED**</dt> </dl>    | Das Besitzerfenster kann Elemente in der Berichtsansicht zeichnen. Das Listenansichtssteuerelement sendet eine [**WM \_ DRAWITEM-Nachricht,**](wm-drawitem.md) um jedes Element zu zeichnen. Es sendet keine separaten Nachrichten für jedes Unterelement. Das **iItemData-Element** der [**DRAWITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) enthält die Elementdaten für das angegebene Listenansichtselement. <br/> |
| <span id="LVS_REPORT"></span><span id="lvs_report"></span><dl> <dt>**\_LVS-BERICHT**</dt> </dl>                            | Dieses Format gibt die Berichtsansicht an. Wenn Sie den LVS \_ REPORT-Stil mit einem Listenansicht-Steuerelement verwenden, wird die erste Spalte immer linksbündig ausgerichtet. Sie können LVCFMT \_ RIGHT nicht verwenden, um diese Ausrichtung zu ändern. Weitere Informationen zur Spaltenausrichtung finden Sie unter [**LVCOLUMN.**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) <br/>                                                                      |
| <span id="LVS_SHAREIMAGELISTS"></span><span id="lvs_shareimagelists"></span><dl> <dt>**LVS \_ SHAREIMAGELISTS**</dt> </dl> | Die Bildliste wird nicht gelöscht, wenn das Steuerelement zerstört wird. Dieser Stil ermöglicht die Verwendung derselben Bildlisten mit mehreren Listenansichtssteuerelementen. <br/>                                                                                                                                                                                          |
| <span id="LVS_SHOWSELALWAYS"></span><span id="lvs_showselalways"></span><dl> <dt>**LVS \_ SHOWSELALWAYS**</dt> </dl>       | Die Auswahl (falls überhaupt) wird immer angezeigt, auch wenn das Steuerelement nicht den Fokus hat. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SINGLESEL"></span><span id="lvs_singlesel"></span><dl> <dt>**LVS \_ SINGLESEL**</dt> </dl>                   | Es kann immer nur ein Element gleichzeitig ausgewählt werden. Standardmäßig können mehrere Elemente ausgewählt werden. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SMALLICON"></span><span id="lvs_smallicon"></span><dl> <dt>**LVS \_ SMALLICON**</dt> </dl>                   | Dieser Stil gibt eine kleine Symbolansicht an. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="LVS_SORTASCENDING"></span><span id="lvs_sortascending"></span><dl> <dt>**LVS \_ SORTASCENDING**</dt> </dl>       | Elementindizes werden nach Elementtext in aufsteigender Reihenfolge sortiert. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="LVS_SORTDESCENDING"></span><span id="lvs_sortdescending"></span><dl> <dt>**LVS \_ SORTDESCENDING**</dt> </dl>    | Elementindizes werden nach Elementtext in absteigender Reihenfolge sortiert. <br/>                                                                                                                                                                                                                                                                                 |
| <span id="LVS_TYPEMASK"></span><span id="lvs_typemask"></span><dl> <dt>**LVS \_ TYPEMASK**</dt> </dl>                      | Bestimmt den aktuellen Fensterstil des Steuerelements. <br/>                                                                                                                                                                                                                                                                                                  |
| <span id="LVS_TYPESTYLEMASK"></span><span id="lvs_typestylemask"></span><dl> <dt>**LVS \_ TYPESTYLEMASK**</dt> </dl>       | Bestimmt die Fensterstile, die die Elementausrichtung sowie die Darstellung und das Verhalten des Headers steuern. <br/>                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Hinweise

Für **die Formate LVS \_ SORTASCENDING** und **LVS \_ SORTDESCENDING** werden Elementindizes basierend auf Elementtext in aufsteigender bzw. absteigender Reihenfolge sortiert. Da die **LVS \_ LIST-** und **LVS \_ REPORT-Ansichten** Elemente in der gleichen Reihenfolge wie ihre Indizes anzeigen, sind die Ergebnisse der Sortierung sofort für den Benutzer sichtbar. Die **LVS \_ ICON-** und **LVS \_ SMALLICON-Ansichten** verwenden keine Elementindizes, um die Position von Symbolen zu bestimmen. Bei diesen Ansichten sind die Ergebnisse der Sortierung für den Benutzer nicht sichtbar.

Sie können die **LVS \_ TYPEMASK-Maske** verwenden, um die Fensterstile zu isolieren, die der aktuellen Ansicht entsprechen: **LVS \_ ICON,** **LVS \_ LIST,** **LVS \_ REPORT** und **LVS \_ SMALLICON**.

Sie können die **LVS \_ ALIGNMASK-Maske** verwenden, um die Fensterformate zu isolieren, die die Ausrichtung von Elementen angeben: **LVS \_ ALIGNLEFT** und **LVS \_ ALIGNTOP**.

Sie können die **LVS \_ TYPESTYLEMASK-Maske** verwenden, um die Fensterstile zu isolieren, die die Elementausrichtung steuern (**LVS \_ ALIGNLEFT** und **LVS \_ ALIGNTOP**) und diejenigen, die die Darstellung und das Verhalten von Headern steuern (**LVS \_ NOCOLUMNHEADER** und **LVS \_ NOSORTHEADER**).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Listenansichtsstile und Ansichten](list-view-controls-overview.md)
</dt> </dl>

 

 





