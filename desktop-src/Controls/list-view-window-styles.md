---
title: List-View Fenster Stile (kommstrg. h)
description: Die folgenden Fenster Stile sind spezifisch für Listenansicht-Steuerelemente.
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
ms.openlocfilehash: cae95bdb8dc1263b485f0bd2c50a8124dd57fc3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356435"
---
# <a name="list-view-window-styles"></a>Fenster Stile List-View

Die folgenden Fenster Stile sind spezifisch für Listenansicht-Steuerelemente.



| Konstante                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVS_ALIGNLEFT"></span><span id="lvs_alignleft"></span><dl> <dt>**LVS \_ alignleft**</dt> </dl>                   | Elemente werden in der Symbol Ansicht und in der kleinen Symbol Ansicht linksbündig ausgerichtet. <br/>                                                                                                                                                                                                                                                                                             |
| <span id="LVS_ALIGNMASK"></span><span id="lvs_alignmask"></span><dl> <dt>**LVS \_ alignmask**</dt> </dl>                   | Die aktuelle Ausrichtung des Steuer Elements. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="LVS_ALIGNTOP"></span><span id="lvs_aligntop"></span><dl> <dt>**LVS \_ AlignTop**</dt> </dl>                      | Elemente werden am oberen Rand des Listenansicht-Steuer Elements in der Symbol Ansicht und in der kleinen Symbol Ansicht ausgerichtet. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_AUTOARRANGE"></span><span id="lvs_autoarrange"></span><dl> <dt>**Automatische Anordnung von LVS \_**</dt> </dl>             | Symbole werden in der Symbol Ansicht und in der kleinen Symbol Ansicht automatisch angeordnet. <br/>                                                                                                                                                                                                                                                                              |
| <span id="LVS_EDITLABELS"></span><span id="lvs_editlabels"></span><dl> <dt>**LVS- \_ EditLabels**</dt> </dl>                | Der Element Text kann direkt bearbeitet werden. Das übergeordnete Fenster muss den [LVN \_ endlabeledit](lvn-endlabeledit.md) -Benachrichtigungs Code verarbeiten. <br/>                                                                                                                                                                                                               |
| <span id="LVS_ICON"></span><span id="lvs_icon"></span><dl> <dt>**LVS- \_ Symbol**</dt> </dl>                                  | Dieser Stil gibt die Symbol Ansicht an. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_LIST"></span><span id="lvs_list"></span><dl> <dt>**LVS- \_ Liste**</dt> </dl>                                  | Dieser Stil gibt die Listenansicht an. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_NOCOLUMNHEADER"></span><span id="lvs_nocolumnheader"></span><dl> <dt>**LVS \_ nocolumnheader**</dt> </dl>    | Spaltenüberschriften werden in der Berichtsansicht nicht angezeigt. Standardmäßig verfügen Spalten über Header in der Berichtsansicht. <br/>                                                                                                                                                                                                                                               |
| <span id="LVS_NOLABELWRAP"></span><span id="lvs_nolabelwrap"></span><dl> <dt>**LVS \_ nolabelwrap**</dt> </dl>             | Der Element Text wird in der Symbol Ansicht in einer einzelnen Zeile angezeigt. Standardmäßig kann der Element Text in der Symbol Ansicht verpackt werden. <br/>                                                                                                                                                                                                                                              |
| <span id="LVS_NOSCROLL"></span><span id="lvs_noscroll"></span><dl> <dt>**LVS \_ NoScroll**</dt> </dl>                      | Der Bildlauf ist deaktiviert. Alle Elemente müssen sich im Client Bereich befinden. Dieser Stil ist nicht kompatibel mit der **LVS- \_ Liste** oder den **LVS- \_ Berichts** Stilen. Weitere Informationen finden Sie im Knowledge Base-Artikel Q137520. <br/>                                                                                                                                      |
| <span id="LVS_NOSORTHEADER"></span><span id="lvs_nosortheader"></span><dl> <dt>**LVS- \_ nosorders**</dt> </dl>          | Spaltenüberschriften funktionieren nicht wie Schaltflächen. Dieser Stil kann verwendet werden, wenn durch Klicken auf eine Spaltenüberschrift in der Berichtsansicht keine Aktion ausgeführt wird, z. b. die Sortierung. <br/>                                                                                                                                                                                       |
| <span id="LVS_OWNERDATA"></span><span id="lvs_ownerdata"></span><dl> <dt>**LVS-Besitzer \_ Daten**</dt> </dl>                   | [Version 4,70](common-control-versions.md). Dieser Stil gibt ein virtuelles Listenansicht-Steuerelement an. Weitere Informationen zu diesem Listen Steuerelement-Stil finden Sie unter Informationen [zu List-View](list-view-controls-overview.md)-Steuerelementen. <br/>                                                                                                                             |
| <span id="LVS_OWNERDRAWFIXED"></span><span id="lvs_ownerdrawfixed"></span><dl> <dt>**LVS \_ besitzdrawfixed**</dt> </dl>    | Das Fenster Besitzer kann Elemente in der Berichtsansicht zeichnen. Das Listenansicht-Steuerelement sendet eine [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht, um jedes Element zu zeichnen. es sendet keine separaten Nachrichten für jedes Unterelement. Der **iitemdata** -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur enthält die Elementdaten für das angegebene Listen Ansichts Element. <br/> |
| <span id="LVS_REPORT"></span><span id="lvs_report"></span><dl> <dt>**LVS- \_ Bericht**</dt> </dl>                            | Dieser Stil gibt die Berichtsansicht an. Bei Verwendung des LVS \_ -Berichts Stils mit einem Listenansicht-Steuerelement wird die erste Spalte immer linksbündig ausgerichtet. Sie können "lvcfmt right" nicht verwenden \_ , um diese Ausrichtung zu ändern. Weitere Informationen zur Spalten Ausrichtung finden Sie unter " [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) ". <br/>                                                                      |
| <span id="LVS_SHAREIMAGELISTS"></span><span id="lvs_shareimagelists"></span><dl> <dt>**LVS \_ shareimagelists**</dt> </dl> | Die Bildliste wird nicht gelöscht, wenn das Steuerelement zerstört wird. Dieser Stil ermöglicht die Verwendung derselben Bildlisten mit mehreren Listenansicht-Steuerelementen. <br/>                                                                                                                                                                                          |
| <span id="LVS_SHOWSELALWAYS"></span><span id="lvs_showselalways"></span><dl> <dt>**LVS \_ showselalways**</dt> </dl>       | Die Auswahl wird, falls vorhanden, immer angezeigt, auch wenn das Steuerelement nicht den Fokus besitzt. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SINGLESEL"></span><span id="lvs_singlesel"></span><dl> <dt>**LVS \_ SingleSel**</dt> </dl>                   | Es kann jeweils nur ein Element ausgewählt werden. Standardmäßig können mehrere Elemente ausgewählt werden. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SMALLICON"></span><span id="lvs_smallicon"></span><dl> <dt>**LVS \_ SmallIcon**</dt> </dl>                   | Dieser Stil gibt eine kleine Symbol Ansicht an. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="LVS_SORTASCENDING"></span><span id="lvs_sortascending"></span><dl> <dt>**LVS \_ SortAscending**</dt> </dl>       | Element Indizes werden basierend auf dem Element Text in aufsteigender Reihenfolge sortiert. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="LVS_SORTDESCENDING"></span><span id="lvs_sortdescending"></span><dl> <dt>**LVS \_ sortsteigend**</dt> </dl>    | Element Indizes werden basierend auf dem Element Text in absteigender Reihenfolge sortiert. <br/>                                                                                                                                                                                                                                                                                 |
| <span id="LVS_TYPEMASK"></span><span id="lvs_typemask"></span><dl> <dt>**LVS- \_ typprägung**</dt> </dl>                      | Bestimmt den aktuellen Fenster Stil des Steuer Elements. <br/>                                                                                                                                                                                                                                                                                                  |
| <span id="LVS_TYPESTYLEMASK"></span><span id="lvs_typestylemask"></span><dl> <dt>**LVS \_ typestylemask**</dt> </dl>       | Bestimmt die Fenster Stile, die die Element Ausrichtung und die Darstellung und das Verhalten des Headers steuern. <br/>                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Bemerkungen

Für **LVS \_ SortAscending** -und **LVS \_ SortAscending** -Stile werden Element Indizes basierend auf dem Element Text in aufsteigender oder absteigender Reihenfolge sortiert. Da die **LVS- \_ Liste** und die **LVS- \_ Berichts** Ansichten Elemente in derselben Reihenfolge wie ihre Indizes anzeigen, sind die Ergebnisse der Sortierung sofort für den Benutzer sichtbar. Das **LVS- \_ Symbol** und die **LVS \_ SmallIcon** -Sichten verwenden keine Element Indizes, um die Position von Symbolen zu bestimmen. Mit diesen Sichten sind die Ergebnisse der Sortierung für den Benutzer nicht sichtbar.

Sie können die **LVS- \_ typemask** -Maske verwenden, um die Fenster Stile zu isolieren, die der aktuellen Ansicht entsprechen: **LVS- \_ Symbol**, **LVS- \_ Liste**, **LVS- \_ Bericht** und **LVS \_ SmallIcon**.

Mit der **LVS \_ alignmask** -Maske können Sie die Fenster Stile isolieren, die die Ausrichtung von Elementen angeben: **LVS \_ alignleft** und **LVS \_ AlignTop**.

Sie können die **LVS \_ typestylemask** mask verwenden, um die Fenster Stile zu isolieren, die die Element Ausrichtung Steuern (**LVS \_ alignleft** und **LVS \_ AlignTop**), und diejenigen, die die Header Darstellung und das Verhalten steuern (**LVS \_ nocolumnheader** und **LVS \_ nosorders**).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Listenansicht: Stile und Ansichten](list-view-controls-overview.md)
</dt> </dl>

 

 





