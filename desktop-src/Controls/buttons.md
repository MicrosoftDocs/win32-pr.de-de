---
title: Schaltfläche (Windows-Steuerelemente)
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Schaltflächen-Steuerelementen verwendet werden. Eine Schaltfläche ist ein Steuerelement, auf das der Benutzer klicken kann, um Eingaben für eine Anwendung bereitzustellen.
ms.assetid: vs|controls|~\controls\buttons\buttons.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babe31ec9f11ee445167e57394da0fa88fd781dd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474829"
---
# <a name="button-windows-controls"></a>Schaltfläche (Windows-Steuerelemente)

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Schaltflächen-Steuerelementen verwendet werden. Eine *Schaltfläche* ist ein Steuerelement, auf das der Benutzer klicken kann, um Eingaben für eine Anwendung bereitzustellen.

### <a name="overviews"></a>Übersichten



| Thema                                       | Inhalte                                                                                                           |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Schaltflächen Meldungen](button-messages.md)      | In diesem Thema werden Meldungen erläutert, die mit Schaltflächen verwendet werden.<br/>                                               |
| [Schaltflächen Zustände](button-states.md)          | In diesem Abschnitt wird erläutert, wie die Auswahl einer Schaltfläche den Zustand und die Reaktion der Anwendung ändert.<br/> |
| [Schaltflächentypen](button-types-and-styles.md) | In diesem Thema werden die unterschiedlichen Arten von Schaltflächen erläutert.<br/>                                                    |
| [Verwenden von Schaltflächen](using-buttons.md)          | In diesem Abschnitt wird erläutert, wie Sie mit Schaltflächen verknüpfte Tasks ausführen.<br/>                            |



 

### <a name="functions"></a>Functions



| Thema                                            | Inhalte                                                                                                                                                                                                  |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Checkdlgbutton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton)         | Ändert den Prüf Zustand eines Schaltflächen-Steuer Elements.<br/>                                                                                                                                                   |
| [**Check RadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)     | Fügt ein angegebenes Optionsfeld in einer Gruppe zu (überprüft) und entfernt alle anderen Options Felder in der Gruppe mit einem Häkchen (löscht). <br/>                                                |
| [**Isdlgbuttoncheck**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) | Die [**isdlgbuttoncheck**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) -Funktion bestimmt, ob ein Schaltflächen-Steuerelement aktiviert ist oder ob ein Schaltflächen-Steuerelement mit drei Zuständen aktiviert, deaktiviert oder unbestimmt ist. <br/> |



 

### <a name="macros"></a>Makros



| Thema                                                                         | Inhalte                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Schaltflächen \_ Aktivierung**](/windows/desktop/api/Windowsx/nf-windowsx-button_enable)                                       | Aktiviert oder deaktiviert eine Schaltfläche.<br/>                                                                                                                                                                                                          |
| [**Schaltfläche \_ getcheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck)                                   | Ruft den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens ab. Sie können dieses Makro verwenden oder die [**BM- \_ getcheck**](bm-getcheck.md) -Nachricht explizit senden. <br/>                                                                                       |
| [**Schaltfläche " \_ getidealsize"**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize)                           | Ruft die Größe der Schaltfläche ab, die am besten zu Text und Bild passt, wenn eine Bildliste vorhanden ist. Sie können dieses Makro verwenden oder die Nachricht [**BCM \_ getidealsize**](bcm-getidealsize.md) explizit senden. <br/>                                      |
| [**Schaltfläche " \_ GetImageList"**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist)                           | Ruft die [**\_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) -Struktur der Schaltfläche ab, die die für ein Schaltflächen-Steuerelement festgelegte Bildliste beschreibt. Sie können dieses Makro verwenden oder die [**BCM \_ GetImageList**](bcm-getimagelist.md) -Nachricht explizit senden. <br/> |
| [**Schaltfläche \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote)                                     | Ruft den Text des Notiz Texts ab, der einer Befehls Link Schaltfläche zugeordnet ist. Sie können dieses Makro verwenden oder die [**BCM \_ GetNote**](bcm-getnote.md) -Nachricht explizit senden.<br/>                                                                            |
| [**Schaltfläche \_ getnotelength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength)                         | Ruft die Länge des Notiz Texts ab, der in der Beschreibung für einen Befehls Link angezeigt werden kann. Verwenden Sie dieses Makro, oder senden Sie die [**BCM- \_ getnotelength**](bcm-getnotelength.md) -Nachricht explizit.<br/>                                           |
| [**Schaltfläche \_ getsplitinfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo)                           | Ruft Informationen für ein angegebenes unterteilte Schaltflächen Steuerelement ab Verwenden Sie dieses Makro, oder senden Sie die [**BCM \_ getsplitinfo**](bcm-getsplitinfo.md) -Nachricht explizit.<br/>                                                                                    |
| [**Schaltfläche \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate)                                   | Ruft den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens ab. Sie können dieses Makro verwenden oder die [**BM- \_ GetState**](bm-getstate.md) -Nachricht explizit senden. <br/>                                                                                       |
| [**Schaltfläche \_ gettext**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettext)                                     | Ruft den Text einer Schaltfläche ab.<br/>                                                                                                                                                                                                             |
| [**Schaltfläche \_ getTextLength**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettextlength)                         | Ruft die Anzahl der Zeichen im Text einer Schaltfläche ab.<br/>                                                                                                                                                                                 |
| [**Schaltfläche \_ gettextmargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin)                         | Ruft die Ränder ab, mit denen Text in einem Schaltflächen-Steuerelement gezeichnet wird. Sie können dieses Makro verwenden oder die [**BCM \_ gettextmargin**](bcm-gettextmargin.md) -Nachricht explizit senden. <br/>                                                                        |
| [**Schaltflächen- \_ setcheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck)                                   | Legt den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens fest. Sie können dieses Makro verwenden oder die [**BM- \_ setcheck**](bm-setcheck.md) -Nachricht explizit senden. <br/>                                                                                       |
| [**Schaltfläche \_ setdropdownstate**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate)                   | Legt den Dropdown-Zustand für eine angegebene Schaltfläche mit dem Format " [**" für das \_**](button-styles.md)Format "" auf Verwenden Sie dieses Makro, oder senden Sie die [**BCM \_ setdropdownstate**](bcm-setdropdownstate.md) -Nachricht explizit. <br/>           |
| [**Schaltfläche " \_ endtelevationrequirements dstate"**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) | Legt den Status der erhöhten Rechte für eine angegebene Schaltfläche oder einen Befehls Link fest, um ein Symbol mit erhöhten Rechten anzuzeigen. Verwenden Sie dieses Makro, oder senden Sie die [**BCM- \_ SETSHIELD**](bcm-setshield.md) -Nachricht explizit. <br/>                                          |
| [**Schaltfläche " \_ SetImageList"**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist)                           | Weist einem Schaltflächen-Steuerelement eine Bildliste zu. Sie können dieses Makro verwenden oder die [**BCM \_ SetImageList**](bcm-setimagelist.md) -Nachricht explizit senden. <br/>                                                                                       |
| [**Schaltflächen- \_ setnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote)                                     | Legt den Text des Hinweises fest, der einer angegebenen Befehls Link Schaltfläche zugeordnet ist. Sie können dieses Makro verwenden oder die [**BCM- \_ setnote**](bcm-setnote.md) -Nachricht explizit senden.<br/>                                                                  |
| [**Schaltfläche \_ setsplitinfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo)                           | Legt Informationen für ein angegebenes Steuerelement für geteilte Schaltflächen fest Verwenden Sie dieses Makro, oder senden Sie die [**BCM- \_ setsplitinfo**](bcm-setsplitinfo.md) -Nachricht explizit.<br/>                                                                                    |
| [**SetState-Schaltfläche \_**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate)                                   | Legt den Hervorhebungs Zustand einer Schaltfläche fest. Der Hervorhebungs Zustand gibt an, ob die Schaltfläche hervorgehoben wird, als ob der Benutzer Sie gedrückt hätte. Sie können dieses Makro verwenden oder die [**BM- \_ SetState**](bm-setstate.md) -Nachricht explizit senden. <br/>        |
| [**Schaltflächen- \_ SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle)                                   | Legt den Stil einer Schaltfläche fest. Sie können dieses Makro verwenden oder die [**BM- \_ SetStyle**](bm-setstyle.md) -Nachricht explizit senden. <br/>                                                                                                                |
| [**Schaltfläche \_ SetText**](/windows/desktop/api/Windowsx/nf-windowsx-button_settext)                                     | Legt den Text einer Schaltfläche fest.<br/>                                                                                                                                                                                                             |
| [**Schaltfläche " \_ settextmargin"**](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)                         | Legt die Ränder zum Zeichnen von Text in einem Schaltflächen-Steuerelement fest. Sie können dieses Makro verwenden oder die [**BCM \_ settextmargin**](bcm-settextmargin.md) -Nachricht explizit senden. <br/>                                                                         |



 

### <a name="messages"></a>Meldungen



| Thema                                                 | Inhalte                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BCM- \_ getidealsize**](bcm-getidealsize.md)         | Ruft die Größe der Schaltfläche ab, die den Text und das Bild am besten anpasst, wenn eine Bildliste vorhanden ist. Sie können diese Nachricht explizit senden oder das [**\_ getidealsize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) -Makro der Schaltfläche verwenden.<br/>                                                                                   |
| [**BCM \_ GetImageList**](bcm-getimagelist.md)         | Ruft die [**\_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) -Struktur der Schaltfläche ab, die die einem Schaltflächen-Steuerelement zugewiesene Bildliste beschreibt. Sie können diese Nachricht explizit senden oder das [**\_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) -Makro der Schaltfläche verwenden.<br/>                                                  |
| [**BCM- \_ GetNote**](bcm-getnote.md)                   | Ruft den Text des Notiz Texts ab, der einer Befehls Link Schaltfläche zugeordnet ist. Sie können diese Nachricht explizit senden oder das [**Schaltfläche \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) -Makro verwenden.<br/>                                                                                                                        |
| [**BCM \_ getnotelength**](bcm-getnotelength.md)       | Ruft die Länge des Notiz Texts ab, der in der Beschreibung für eine Befehls Link Schaltfläche angezeigt werden kann. Senden Sie diese Nachricht explizit oder mithilfe der [**Schaltfläche \_ getnotelength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) -Makro.<br/>                                                                           |
| [**BCM \_ getsplitinfo**](bcm-getsplitinfo.md)         | Ruft Informationen für ein unterteilte Schaltflächen Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**Schaltflächen \_ getsplitinfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) -Makros. <br/>                                                                                                                                    |
| [**BCM \_ gettextmargin**](bcm-gettextmargin.md)       | Ruft die Ränder ab, mit denen Text in einem Schaltflächen-Steuerelement gezeichnet wird. Sie können diese Nachricht explizit senden oder das [**\_ gettextmargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) -Makro der Schaltfläche verwenden.<br/>                                                                                                                     |
| [**BCM \_ setdropdownstate**](bcm-setdropdownstate.md) | Legt den Dropdown-Zustand für eine Schaltfläche mit dem [**\_ Dropdown Menü Style tbstyle**](toolbar-control-and-button-styles.md)fest. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ setdropdownstate**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) -Makros der Schaltfläche.<br/>                                        |
| [**BCM \_ SetImageList**](bcm-setimagelist.md)         | Weist einem Schaltflächen-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit senden oder das [**\_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) -Makro der Schaltfläche verwenden.<br/>                                                                                                                                    |
| [**BCM- \_ setnote**](bcm-setnote.md)                   | Legt den Text des Hinweises fest, der einer Befehls Link Schaltfläche zugeordnet ist. Sie können diese Nachricht explizit senden oder das Schaltflächen- [**\_ setnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) -Makro verwenden.<br/>                                                                                                                        |
| [**BCM- \_ SETSHIELD**](bcm-setshield.md)               | Legt den Status der erhöhten Rechte für eine angegebene Schaltfläche oder einen Befehls Link fest, um ein Symbol mit erhöhten Rechten anzuzeigen. Senden Sie diese Nachricht explizit oder mithilfe des [**Schalt \_**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) Flächen-Makros "".<br/>                                                  |
| [**BCM \_ setsplitinfo**](bcm-setsplitinfo.md)         | Legt Informationen für ein unterteilte Schaltflächen Steuerelement fest. Senden Sie diese Nachricht explizit oder mithilfe der [**Schaltfläche \_ setsplitinfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) -Makro.<br/>                                                                                                                                     |
| [**BCM \_ settextmargin**](bcm-settextmargin.md)       | Die [**BCM \_ settextmargin**](bcm-settextmargin.md) -Meldung legt die Ränder zum Zeichnen von Text in einem Schaltflächen-Steuerelement fest. <br/>                                                                                                                                                                      |
| [**BM- \_ Click**](bm-click.md)                         | Simuliert den Benutzer, der auf eine Schaltfläche klickt. Diese Meldung bewirkt, dass die Schaltfläche [**die \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -und die [**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldungen empfängt [ \_](bn-clicked.md)<br/> |
| [**BM \_ getcheck**](bm-getcheck.md)                   | Ruft den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens ab. Sie können diese Nachricht explizit senden oder das [**Schaltfläche \_ getcheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) -Makro verwenden.<br/>                                                                                                                                  |
| [**BM- \_ GetImage**](bm-getimage.md)                   | Ruft ein Handle für das Bild (Symbol oder Bitmap) ab, das der Schaltfläche zugeordnet ist.<br/>                                                                                                                                                                                                             |
| [**BM \_ GetState**](bm-getstate.md)                   | Ruft den Zustand einer Schaltfläche oder eines Kontrollkästchens ab. Sie können diese Nachricht explizit senden oder das [**\_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) -Makro der Schaltfläche verwenden.<br/>                                                                                                                                         |
| [**BM- \_ setcheck**](bm-setcheck.md)                   | Legt den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens fest. Sie können diese Nachricht explizit oder mithilfe des Schaltflächen [**\_ setcheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) -Makros senden.<br/>                                                                                                                             |
| [**BM \_ setdontclick**](bm-setdontclick.md)           | Legt ein Flag für ein Optionsfeld fest, das die Generierung [von \_ Milliarden](bn-clicked.md) -Nachrichten steuert, wenn die Schaltfläche den Fokus erhält.<br/>                                                                                                                                                     |
| [**BM- \_ Zeitrahmen**](bm-setimage.md)                   | Verknüpft ein neues Bild (Symbol oder Bitmap) mit der Schaltfläche.<br/>                                                                                                                                                                                                                                 |
| [**BM \_ SetState**](bm-setstate.md)                   | Legt den Hervorhebungs Zustand einer Schaltfläche fest. Der Hervorhebungs Zustand gibt an, ob die Schaltfläche hervorgehoben wird, als ob der Benutzer Sie gedrückt hätte. Sie können diese Nachricht explizit senden oder das [**\_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) -Makro der Schaltfläche verwenden.<br/>                                                   |
| [**BM- \_ SetStyle**](bm-setstyle.md)                   | Legt den Stil einer Schaltfläche fest. Sie können diese Nachricht explizit senden oder das [**\_ SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) -Makro der Schaltfläche verwenden.<br/>                                                                                                                                                           |



 

### <a name="notifications"></a>Benachrichtigungen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>Inhalte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="bcn-dropdown.md">BCN_DROPDOWN</a></td>
<td>Wird gesendet, wenn der Benutzer auf einen Dropdown Pfeil auf einer Schaltfläche klickt. Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code in Form einer <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> Nachricht.<br/></td>
</tr>
<tr class="even">
<td><a href="bcn-hotitemchange.md">BCN_HOTITEMCHANGE</a></td>
<td>Benachrichtigt den Besitzer des Button-Steuer Elements, dass die Maus in den Client Bereich des Schaltflächen-Steuer Elements wechselt oder diesen verlässt. Das Schaltflächen-Steuerelement sendet diesen Benachrichtigungs Code in Form einer <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> Nachricht.<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-clicked.md">BN_CLICKED</a></td>
<td>Wird gesendet, wenn der Benutzer auf eine Schaltfläche klickt. <br/> Das übergeordnete Fenster der Schaltfläche empfängt den <a href="bn-clicked.md">BN_CLICKED</a> Benachrichtigungs Code über die <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Nachricht. <br/></td>
</tr>
<tr class="even">
<td><a href="bn-dblclk.md">BN_DBLCLK</a></td>
<td>Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt. Dieser Benachrichtigungs Code wird automatisch für <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>-, <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a>-und <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> -Schaltflächen gesendet. Andere Schaltflächen Typen senden nur <a href="bn-dblclk.md">BN_DBLCLK</a> , wenn Sie den <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> Formatvorlagen aufweisen.<br/> Das übergeordnete Fenster der Schaltfläche empfängt den <a href="bn-dblclk.md">BN_DBLCLK</a> Benachrichtigungs Code über die <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Nachricht. <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-disable.md">BN_DISABLE</a></td>
<td>Wird gesendet, wenn eine Schaltfläche deaktiviert ist.
<blockquote>
[!Note]<br />
Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt. Anwendungen sollten den <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> Schaltflächen Stil und die <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>drawitemstruct</strong></a> -Struktur für diese Aufgabe verwenden.
</blockquote>
<br/> <br/> Das übergeordnete Fenster der Schaltfläche empfängt den <a href="bn-disable.md">BN_DISABLE</a> Benachrichtigungs Code über die <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Nachricht.<br/></td>
</tr>
<tr class="even">
<td><a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a></td>
<td>Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt. Dieser Benachrichtigungs Code wird automatisch für <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>-, <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a>-und <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> -Schaltflächen gesendet. Andere Schaltflächen Typen senden nur <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> , wenn Sie den <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> Formatvorlagen aufweisen.<br/> Das übergeordnete Fenster der Schaltfläche empfängt den <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> Benachrichtigungs Code über die <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Nachricht. <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-hilite.md">BN_HILITE</a></td>
<td>Wird gesendet, wenn der Benutzer eine Schaltfläche auswählt.
<blockquote>
[!Note]<br />
Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt. Anwendungen sollten den <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> Schaltflächen Stil und die <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>drawitemstruct</strong></a> -Struktur für diese Aufgabe verwenden.
</blockquote>
<br/> <br/> Das übergeordnete Fenster der Schaltfläche empfängt den <a href="bn-hilite.md">BN_HILITE</a> Benachrichtigungs Code über die <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Nachricht.<br/></td>
</tr>
<tr class="even">
<td><a href="bn-killfocus.md">BN_KILLFOCUS</a></td>
<td>Wird gesendet, wenn eine Schaltfläche den Tastaturfokus verliert. Die Schaltfläche muss den <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> Stil aufweisen, um diesen Benachrichtigungs Code zu senden. <br/> Das übergeordnete Fenster der Schaltfläche empfängt den <a href="bn-killfocus.md">BN_KILLFOCUS</a> Benachrichtigungs Code über die <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Nachricht. <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-paint.md">BN_PAINT</a></td>
<td>Wird gesendet, wenn eine Schaltfläche gezeichnet werden soll.
<blockquote>
[!Note]<br />
Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt. Anwendungen sollten den <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> Schaltflächen Stil und die <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>drawitemstruct</strong></a> -Struktur für diese Aufgabe verwenden.
</blockquote>
<br/> <br/> Das übergeordnete Fenster der Schaltfläche empfängt den <a href="bn-paint.md">BN_PAINT</a> Benachrichtigungs Code über die <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Nachricht. <br/></td>
</tr>
<tr class="even">
<td><a href="bn-pushed.md">BN_PUSHED</a></td>
<td>Wird gesendet, wenn der pushzustand einer Schaltfläche auf Push festgelegt ist.
<blockquote>
[!Note]<br />
Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt. Anwendungen sollten den <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> Schaltflächen Stil und die <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>drawitemstruct</strong></a> -Struktur für diese Aufgabe verwenden.
</blockquote>
<br/> <br/> Das übergeordnete Fenster der Schaltfläche empfängt den <a href="bn-pushed.md">BN_PUSHED</a> Benachrichtigungs Code über die <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Nachricht.<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-setfocus.md">BN_SETFOCUS</a></td>
<td>Wird gesendet, wenn eine Schaltfläche den Tastaturfokus erhält. Die Schaltfläche muss den <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> Stil aufweisen, um diesen Benachrichtigungs Code zu senden. <br/> Das übergeordnete Fenster der Schaltfläche empfängt den <a href="bn-setfocus.md">BN_SETFOCUS</a> Benachrichtigungs Code über die <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Nachricht.<br/></td>
</tr>
<tr class="even">
<td><a href="bn-unhilite.md">BN_UNHILITE</a></td>
<td>Wird gesendet, wenn die Hervorhebung aus einer Schaltfläche entfernt werden soll.
<blockquote>
[!Note]<br />
Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt. Anwendungen sollten den <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> Schaltflächen Stil und die <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>drawitemstruct</strong></a> -Struktur für diese Aufgabe verwenden.
</blockquote>
<br/> <br/> Das übergeordnete Fenster der Schaltfläche empfängt den <a href="bn-unhilite.md">BN_UNHILITE</a> Benachrichtigungs Code über die <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Nachricht.<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-unpushed.md">BN_UNPUSHED</a></td>
<td>Wird gesendet, wenn der pushzustand einer Schaltfläche auf nicht per Push übertragen festgelegt ist.
<blockquote>
[!Note]<br />
Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt. Anwendungen sollten den <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> Schaltflächen Stil und die <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>drawitemstruct</strong></a> -Struktur für diese Aufgabe verwenden.
</blockquote>
<br/> <br/> Das übergeordnete Fenster der Schaltfläche empfängt den <a href="bn-unpushed.md">BN_UNPUSHED</a> Benachrichtigungs Code über die <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Nachricht.<br/></td>
</tr>
<tr class="even">
<td><a href="nm-customdraw-button.md">NM_CUSTOMDRAW (Schaltfläche)</a></td>
<td>Benachrichtigt das übergeordnete Fenster eines Schaltflächen-Steuer Elements über benutzerdefinierte Zeichnungsvorgänge auf der Schaltfläche. <br/> Das Schaltflächen-Steuerelement sendet diesen Benachrichtigungs Code in Form einer <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> Nachricht.<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a></td>
<td>Die <a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a> Meldung wird vor dem Zeichnen der Schaltfläche an das übergeordnete Fenster einer Schaltfläche gesendet. Das übergeordnete Fenster kann die Text-und Hintergrundfarben der Schaltfläche ändern. Allerdings reagieren nur vom Besitzer gezeichnete Schaltflächen auf das übergeordnete Fenster, das diese Nachricht verarbeitet. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a>Strukturen



| Thema                                         | Inhalte                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Schaltflächen- \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) | Enthält Informationen über eine Bildliste, die mit einem Schaltflächen-Steuerelement verwendet wird.<br/>                                                                                                                                                                                                                                 |
| [**Schaltflächen \_ splitinfo**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) | Enthält Informationen, die eine unterteilte Schaltfläche definieren (die Typen [**\_ SplitButton**](button-styles.md) und [**SB \_ defsplitbutton**](button-styles.md) -Stile). Wird mit den [**BCM \_ getsplitinfo**](bcm-getsplitinfo.md) -und [**BCM \_ setsplitinfo**](bcm-setsplitinfo.md) -Meldungen verwendet.<br/> |
| [**Nmbcdropdown**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown)          | Enthält Informationen zu einer [BCN- \_ Dropdown](bcn-dropdown.md) Benachrichtigung.<br/>                                                                                                                                                                                                                                 |
| [**Nmbchotitem**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)            | Enthält Informationen über die Bewegung des Mauszeigers über ein Schaltflächen-Steuerelement.<br/>                                                                                                                                                                                                                                  |



 

### <a name="constants"></a>Konstanten



| Thema                              | Inhalte                                                                                                                                                                                                                                                            |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Schaltflächenstile](button-styles.md) | Gibt eine Kombination von Schaltflächen Stilen an. Wenn Sie eine Schaltfläche mithilfe der Schaltflächen Klasse mit der Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " erstellen, können Sie einen der unten aufgeführten Schaltflächenstile angeben.<br/> |



 

