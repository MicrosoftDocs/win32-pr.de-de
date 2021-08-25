---
description: Das InkPicture-Steuerelement bietet die Möglichkeit, ein Bild in einer Anwendung zu platzieren und Benutzern das Hinzufügen von Ink-Daten darüber zu ermöglichen.
ms.assetid: e9fa6807-6e2a-44ec-9b8f-a560185e4367
title: InkPicture-Steuerelementreferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93f5727d2f3f049a579e32e5feb0ba0eaa742d2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471536"
---
# <a name="inkpicture-control-reference"></a>InkPicture-Steuerelementreferenz

Das InkPicture-Steuerelement bietet die Möglichkeit, ein Bild in einer Anwendung zu platzieren und Benutzern das Hinzufügen von Ink-Daten darüber zu ermöglichen. Sie ist für Szenarien vorgesehen, in denen Ink nicht als Text erkannt, sondern stattdessen als Ink gespeichert wird.

Das InkPicture-Steuerelement kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

> [!Note]  
> Das InkPicture-Steuerelement ist für die Skripterstellung nicht als sicher markiert. Das InkPicture-Steuerelement sollte nicht in HTML- oder ASP.NET werden.

 

Das Erstellen des InkPicture-Steuerelements hinter einem transparenten Steuerelement (z. B. eine GroupBox mit dem WS EX TRANSPARENT-Eigenschaftensatz) verhindert, dass \_ \_ InkPicture InkPicture sammelt.

## <a name="members"></a>Member



| Enumeration                                      | Beschreibung                                                                                              |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InkPictureSizeMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpicturesizemode) | Definiert Werte, die angeben, wie sich das Hintergrundbild innerhalb des InkPicture-Steuerelements verhält.<br/> |



 



| Ereignis                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ChangeUICues**                                                                   | Veraltet.<br/>                                                                                                                                                                                                                                                                                             |
| [**Klicken**](inkpicture-click.md)                                                  | Tritt ein, wenn ein Benutzer auf das InkPicture-Steuerelement klickt.<br/>                                                                                                                                                                                                                                                       |
| [**CursorButtonDown-Ereignis**](inkpicture-cursorbuttondown.md)                      | Tritt ein, wenn das [**InkCollector-Steuerelement**](inkcollector-class.md) ein [**heruntergefahrenes IInkCursorButton-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) erkennt.<br/>                                                                                                                                                         |
| [**CursorButtonUp-Ereignis**](inkpicture-cursorbuttonup.md)                          | Tritt ein, wenn das InkPicture-Steuerelement einen [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) erkennt, der in Der Fall ist.<br/>                                                                                                                                                                                                  |
| [**CursorDown-Ereignis**](inkpicture-cursordown.md)                                  | Tritt ein, wenn die Cursorspitze die digitalisierende Tablet-Oberfläche kontaktiert.<br/>                                                                                                                                                                                                                                      |
| [**CursorInRange-Ereignis**](inkpicture-cursorinrange.md)                            | Tritt ein, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tablet-Kontexts eintritt.<br/>                                                                                                                                                                                                             |
| [**CursorOutOfRange-Ereignis**](inkpicture-cursoroutofrange.md)                      | Tritt ein, wenn der Cursor den physischen Erkennungsbereich (Näherung) des Tablet-Kontexts verlässt.<br/>                                                                                                                                                                                                           |
| [**Dblclick**](inkpicture-dblclick.md)                                            | Tritt ein, wenn auf das InkPicture-Steuerelement doppelklickt.<br/> Diese Ereignismethode wird in der **\_ IInkPictureEvents-Schnittstelle** definiert. Die **\_ IInkPictureEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IPEDblClick.<br/> |
| [**Gestenereignis**](inkpicture-gesture.md)                                        | Tritt ein, wenn eine Anwendungsgeste erkannt wird.<br/>                                                                                                                                                                                                                                                       |
| [**\[KeyDown-Ereignis-InkPicture-Steuerelement\]**](inkpicture-keydown.md)                 | Tritt ein, wenn eine Taste gedrückt wird und sich in der nach unten positionierten Position befindet, während das InkPicture-Steuerelement den Fokus besitzt.<br/>                                                                                                                                                                                                           |
| [**\[KeyPress-Ereignis-InkPicture-Steuerelement\]**](inkpicture-keypress.md)                | Tritt ein, wenn eine Taste gedrückt wird, während das InkPicture-Steuerelement den Fokus besitzt.<br/>                                                                                                                                                                                                                                    |
| [**\[KeyUp-Ereignis-InkPicture-Steuerelement\]**](inkpicture-keyup.md)                     | Tritt ein, wenn eine Taste freigegeben wird, während das InkPicture-Steuerelement den Fokus besitzt.<br/>                                                                                                                                                                                                                                   |
| [**\[MouseDown-Ereignis-InkPicture-Steuerelement\]**](inkpicture-mousedown.md)             | Tritt ein, wenn sich der Mauszeiger über dem InkPicture-Steuerelement befindet und eine Maustaste gedrückt wird.<br/>                                                                                                                                                                                                             |
| [**Mouseenter**](inkpicture-mouseenter.md)                                        | Tritt ein, wenn der Mauszeiger in das InkPicture-Steuerelement eintritt.<br/>                                                                                                                                                                                                                                            |
| [**MouseHover**](inkpicture-mousehover.md)                                        | Tritt ein, wenn der Mauszeiger mit dem Mauszeiger auf das InkPicture-Steuerelement zeigen kann.<br/>                                                                                                                                                                                                                                       |
| [**MouseLeave**](inkpicture-mouseleave.md)                                        | Tritt ein, wenn der Mauszeiger das InkPicture-Steuerelement verlässt.<br/>                                                                                                                                                                                                                                            |
| [**\[MouseMove-Ereignis-InkPicture-Steuerelement\]**](inkpicture-mousemove.md)             | Tritt ein, wenn der Mauszeiger über das InkPicture-Steuerelement bewegt wird.<br/>                                                                                                                                                                                                                                     |
| [**\[MouseUp-Ereignis-InkPicture-Steuerelement\]**](inkpicture-mouseup.md)                 | Tritt ein, wenn sich der Mauszeiger über dem InkPicture-Steuerelement befindet und eine Maustaste losgelassen wird.<br/>                                                                                                                                                                                                            |
| [**Mousewheel**](inkpicture-mousewheel.md)                                        | Tritt ein, wenn sich das Mausrad bewegt, während das InkPicture-Steuerelement den Fokus besitzt.<br/>                                                                                                                                                                                                                               |
| [**NewInAirPackets-Ereignis**](inkpicture-newinairpackets.md)                        | Tritt ein, wenn ein Paket in der Luft gesehen wird.<br/>                                                                                                                                                                                                                                                                   |
| [**NewPackets-Ereignis**](inkpicture-newpackets.md)                                  | Tritt ein, wenn das InkPicture-Steuerelement ein Paket empfängt.<br/>                                                                                                                                                                                                                                                   |
| [**Gemalt**](inkpicture-painted.md)                                              | Tritt ein, wenn das InkPicture-Steuerelement die Neuzeichnung selbst abgeschlossen hat.<br/>                                                                                                                                                                                                                                      |
| [**Malerei**](inkpicture-painting.md)                                            | Tritt ein, bevor das InkPicture-Steuerelement sich selbst neu gedrammt.<br/>                                                                                                                                                                                                                                                    |
| [**Größe ändern**](inkpicture-resize.md)                                                | Tritt ein, wenn die Größe des InkPicture-Steuerelements geändert wird.<br/>                                                                                                                                                                                                                                                          |
| [**SelectionChanged**](inkpicture-selectionchanged.md)                            | Tritt ein, wenn sich die Textauswahl im InkPicture-Steuerelement geändert hat, z. B. durch [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) Änderungen an der Benutzeroberfläche, Durchschneide- und Einfügevorgänge oder die Selection-Eigenschaft.<br/>                                                                                    |
| [**Selectionchanging**](inkpicture-selectionchanging.md)                          | Tritt ein, wenn sich die Textauswahl im InkPicture-Steuerelement ändert, z. B. durch Änderungen an [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) der Benutzeroberfläche, Durchschneide- und Einfügevorgänge oder die Selection-Eigenschaft.<br/>                                                                             |
| [**Selectionmoved**](inkpicture-selectionmoved.md)                                | Tritt ein, wenn sich die Position der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die [**Selection-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                                  |
| [**\[SelectionMoving-EreignisinkPicture-Steuerelement\]**](inkpicture-selectionmoving.md) | Tritt ein, wenn sich die Position der aktuellen Auswahl ändert, z. B. durch Änderungen an der Benutzeroberfläche, Durchschneide- und Einfügevorgänge oder die [**Selection-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                           |
| [**Selectionresized**](inkpicture-selectionresized.md)                            | Tritt ein, wenn sich die Größe der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die [**Selection-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                                      |
| [**Selectionresizing**](inkpicture-selectionresizing.md)                          | Tritt ein, wenn sich die Größe der aktuellen Auswahl ändern wird, z. B. durch Änderungen [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die Selection-Eigenschaft.<br/>                                                                                               |
| [**SizeChanged**](inkpicture-sizechanged.md)                                      | Tritt ein, nachdem die Größe des InkPicture-Steuerelements geändert wurde, insbesondere nachdem sich der [**Width-**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) oder [**Height-Eigenschaftswert**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) geändert hat.<br/>                                                                                                      |
| [**SizeModeChanged**](inkpicture-sizemodechanged.md)                              | Tritt ein, nachdem die [**SizeMode-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) des InkPicture-Steuerelements geändert wurde.<br/>                                                                                                                                                                                           |
| **StyleChanged**                                                                   | Nicht implementiert.<br/>                                                                                                                                                                                                                                                                                        |
| [**Takt**](inkpicture-stroke.md)                                                | Tritt ein, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.<br/>                                                                                                                                                                                                                                                  |
| [**Striche gelöscht**](inkpicture-strokesdeleted.md)                                | Tritt ein, nachdem [**IInkStrokeDisp-Objekte**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) aus der [**Ink-Eigenschaft gelöscht**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) wurden.<br/>                                                                                                                                                                        |
| [**StrokesDeleting**](inkpicture-strokesdeleting.md)                              | Tritt ein, bevor [**IInkStrokeDisp-Objekte**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) aus der [**Ink-Eigenschaft gelöscht**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) werden.<br/>                                                                                                                                                                             |
| [**SystemColorsChanged**](inkpicture-systemcolorschanged.md)                      | Tritt ein, nachdem sich die Systemfarben geändert haben.<br/>                                                                                                                                                                                                                                                                  |
| [**Systemgesture**](inkpicture-systemgesture.md)                                  | Tritt ein, wenn eine Systemgeste erkannt wird.<br/>                                                                                                                                                                                                                                                             |
| [**TabletAdded-Ereignis**](inkpicture-tabletadded.md)                                | Tritt ein, wenn dem System ein Tablet hinzugefügt wird.<br/>                                                                                                                                                                                                                                                            |
| [**TabletRemoved-Ereignis**](inkpicture-tabletremoved.md)                            | Tritt ein, wenn ein Tablet aus dem System entfernt wird.<br/>                                                                                                                                                                                                                                                        |



 



| Methode                                                                                   | BESCHREIBUNG                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetEventInterest-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | Gibt einen Wert zurück, der angibt, ob das InkPicture-Steuerelement für ein bestimmtes Ereignis von Interesse ist.<br/>                                                                   |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | Gibt einen Wert zurück, der angibt, ob das InkPicture-Steuerelement an einer bestimmten Anwendungsgeste interessiert ist.<br/>                                                     |
| [**GetWindowInputRectangle-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | Gibt das Fensterrechteck in Pixel zurück, in dem Ink gezeichnet wird.<br/>                                                                                                 |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | Gibt einen Member der [**SelectionHitResult-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) zurück, der angibt, welcher Teil einer Auswahl bei einem Treffertest erreicht wurde (sofern ein Teil davon) erreicht wurde.<br/> |
| [**SetAllTabletsMode-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | Ermöglicht es dem InkPicture-Steuerelement, InkPicture von jedem Tablet zu erfassen, das an den Tablet-PC angeschlossen ist.<br/>                                                                            |
| [**SetEventInterest-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | Legt einen Wert fest, der angibt, ob ein InkPicture-Steuerelement an einem angegebenen Ereignis interessiert ist.<br/>                                                                        |
| SetFocus                                                                                 | Verschiebt den Fokus auf das InkPicture-Steuerelement.<br/>                                                                                                                          |
| [**SetGestureStatus-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | Legt das Interesse des InkPicture-Objekts in einer angegebenen Anwendungsgeste fest.<br/>                                                                                      |
| [**SetSingleTabletIntegratedMode-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | Legt das InkPicture-Steuerelement so fest, dass Es nur Von einem Tablet, das an den Tablet-PC angefügt ist, InkPicture erfasst. Ink von anderen Tablets wird ignoriert.<br/>                                       |
| [**SetWindowInputRectangle-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | Gibt das Fensterrechteck an, das in Fensterkoordinaten festgelegt werden soll, in dem Ink gezeichnet wird.<br/>                                                                            |
| ShowWhatsThis                                                                            | Zeigt ein ausgewähltes Thema in einer Hilfedatei mithilfe des Popupfensters "What es This" an, das von der Hilfe in 32-Bit-Microsoft Windows-Betriebssystemen bereitgestellt wird (nur Zur Entwurfszeit).<br/>           |
| Zorder                                                                                   | Platziert das Steuerelement an der Vorder- oder Rückseite der Z-Reihenfolge innerhalb seiner grafischen Ebene (nur Entwurfszeit).<br/>                                                               |



 




| Eigenschaft | BESCHREIBUNG | 
|----------|-------------|
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw-Eigenschaft</strong></a> | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob das InkPicture-Steuerelement neu gezeichnet wird, wenn das Fenster ungültig wird (ob das derzeit dem InkPicture-Steuerelement zugeordnete <a href="inkdisp-class.md"><strong>InkDisp-Objekt</strong></a> automatisch neu gezeichnet wird, wenn das der InkPicture zugeordnete Fenster eine WM_PAINT-Nachricht empfängt).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>Backcolor</strong></a> | Ruft die Hintergrundfarbe für das InkPicture-Steuerelement ab oder legt diese fest. Die Standardhintergrundfarbe ist die Hintergrundfarbe des Systemfensters, die in der Regel weiß ist.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk-Eigenschaft</strong></a> | Ruft den Wert ab, der angibt, ob das InkPicture-Steuerelement InkPicture (nur Laufzeit) sammelt.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a> | Ruft den Auflistungsmodus ab, der bestimmt, ob Dieb-, Gesten- oder Ink- und Gesten beim Schreiben durch den Benutzer erkannt werden, oder legt diesen fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors-Eigenschaft</strong></a> | Ruft die <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors-Auflistung</strong></a> ab, die für die Verwendung im Freiraumbereich des InkPicture-Steuerelements verfügbar ist.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>Customstrokes</strong></a> | Ruft die <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes-Auflistung</strong></a> ab, die mit der Ink-Auflistung beibehalten werden soll (nur zur Entwurfszeit).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes-Eigenschaft</strong></a> | Ruft die standardmäßige <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes-Auflistung</strong></a> ab, die beim Zeichnen und Anzeigen von Ink (nur Laufzeit) verwendet werden soll, oder legt diese fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription-Eigenschaft</strong></a> | Ruft die Paketbeschreibung des InkPicture-Steuerelements ab (nur Laufzeit), oder legt sie fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering-Eigenschaft</strong></a> | Ruft den Wert ab, der angibt, ob das InkPicture-Steuerelement die InkPicture-Eigenschaft dynamisch rendert, während sie gesammelt wird, oder legt diesen fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>Editingmode</strong></a> | Ruft einen Wert ab, der angibt, ob sich das InkPicture-Steuerelement im InkPicture-Modus, im Löschmodus oder im Auswahl-/Bearbeitungsmodus befindet, oder legt diesen fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Aktiviert</strong></a> | Ruft einen Wert ab, der bestimmt, ob das InkPicture-Steuerelement auf vom Benutzer generierte Ereignisse reagieren kann, oder legt diesen fest.<br /><blockquote>[!Note]<br />Diese Eigenschaft entspricht der <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled-Eigenschaft.</strong></a></blockquote><br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a> | Ruft den Wert ab, der angibt, ob die Ink-Eigenschaft per Strich oder Punkt gelöscht wird, oder legt diesen fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a> | Ruft den Wert ab, der die Breite der Radiererstiftspitze angibt, oder legt diesen fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>Hwnd</strong></a> | Ruft das Fensterhandler ab, an das das InkPicture-Steuerelement gebunden ist. (nur Laufzeit)<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Freihand</strong></a> | Ruft das <a href="inkdisp-class.md"><strong>InkDisp-Objekt ab,</strong></a> das dem InkPicture-Steuerelement zugeordnet ist (nur Laufzeit), oder legt dieses fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>Inkenabled</strong></a> | Ruft einen Wert ab, der angibt, ob das InkPicture-Steuerelement Stifteingaben erfasst (In-Air-Pakete, Cursor in Bereichsereignissen und so weiter), oder legt diesen fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX-Eigenschaft</strong></a> | Ruft den X-Achsenrand um das Fensterrechteck in Bildschirmkoordinaten ab oder legt ihn fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY-Eigenschaft</strong></a> | Ruft den Rand der y-Achse um das Fensterrechteck in Bildschirmkoordinaten ab oder legt ihn fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon-Eigenschaft</strong></a> | Ruft das aktuelle benutzerdefinierte Maussymbol ab oder legt es fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer-Eigenschaft</strong></a> | Ruft einen Wert ab, der den Typ des Mauszeigers angibt, der angezeigt wird, wenn sich die Maus über einem bestimmten Teil des InkPicture-Steuerelements befindet, oder legt diesen fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Bild</strong></a> | Ruft die Grafikdatei ab, die im InkPicture-Steuerelement angezeigt werden soll.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer-Eigenschaft</strong></a> | Ruft das <a href="inkrenderer-class.md"><strong>InkRenderer-Objekt</strong></a> ab, das zum Zeichnen von InkPicture-Steuerelementen verwendet wird (nur Laufzeit), oder legt dieses fest.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Auswahl</strong></a> | Ruft die <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes-Auflistung</a> ab, die derzeit im InkPicture-Steuerelement ausgewählt ist (nur Laufzeit).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>Größenanpassung</strong></a> | Ruft ab oder legt fest, wie das Steuerelement die Bildplatzierung und -größe behandelt.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk-Eigenschaft</strong></a> | Ruft einen Wert ab, der angibt, ob Ink als nur eine Farbe gerendert wird: Color = COLOR_WINDOWTEXT (aus dem GetSystemMetrics-Aufruf), wenn sich das System im hoher Kontrast befindet.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a> | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob alle Auswahlbenutzeroberflächen (auswahlgebundenes Feld und Auswahlhandles) in hohem Kontrast gezeichnet werden, wenn sich das System im hoher Kontrast befindet.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Tablet-Eigenschaft</strong></a> | Ruft das <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet-Objekt</strong></a> ab, das das InkPicture-Steuerelement derzeit zum Erfassen von Eingaben verwendet.<br /> | 




 

## <a name="remarks"></a>Hinweise

Die Laufzeitbenutzeroberfläche für das InkPicture-Steuerelement ist ein Fenster mit einem nicht transparenten Hintergrund (einzelne Farbe, Bildhintergrund oder beides), das nicht transparente Ink-Farben enthält.

Sie können das InkPicture-Steuerelement verwenden, um Ink in Microsoft Windows 2000, Windows Server 2003, einer anderen Edition von Windows XP als Windows XP Tablet PC Edition und einer beliebigen Version von Windows Vista zu rendern. Sie können jedoch Ink eingeben, Gesten akzeptieren oder Handschrift nur unter den folgenden Bedingungen erkennen:

-   Ink kann eingegeben und erkannt werden, wenn Windows Vista oder XP Tablet PC Edition 2005 installiert ist.
-   Gesten können auch erkannt werden.
-   Handschrift kann als Text erkannt werden, wenn die Handschrift von Computern stammt, auf denen ältere Versionen von Windows, solange Wiedererkennungen vorhanden sind.

Wenn Sie Windows 2000, Windows Server 2003, eine beliebige Edition von Windows XP mit Einer anderen Version als Windows XP Tablet PC Edition 2005, verwenden, können Sie den Umgebungseigenschaften des InkPicture-Steuerelements Werte zuweisen und diese anschließend in andere Anwendungen kopieren und einfügen. Der Wert der InkEnabled-Eigenschaft ist jedoch immer **FALSE.**

Persistente [**InkDisp-Objekte**](inkdisp-class.md) können in allen Editionen von Windows Vista und XP sowie auf Systemen geladen und angezeigt werden, auf denen nur das Windows XP Tablet PC Edition Software Development Kit (SDK) installiert ist. **InkDisp-Objekte** können nur in Text konvertiert (erkannt) werden, wenn Windows Vista oder Windows XP Tablet PC Edition 2005 installiert ist.

Wenn Vorgänge für dieses Steuerelement nicht erfolgreich sind, wird ein rechtliches HRESULT zurückgegeben. Wenn Fehlerbedingungen entstehen, überprüfen Sie das zurückgegebene HRESULT auf den Fehler.

Weitere Informationen zu Ink-Steuerelementen finden Sie unter [Ink](ink-controls.md).

Informationen dazu, welche Threads bestimmte Ereignisse ausdehnen, finden Sie unter Threads, für [die ein Ereignis ausgeführt werden kann.](threads-on-which-an-event-can-fire.md)

Um die Leistung Ihrer Anwendung zu verbessern, löschen Sie manuell ein InkPicture-Steuerelement, wenn es nicht mehr benötigt wird.

> [!Note]  
> Wenn ein InkPicture-Steuerelement mit einem anderen Steuerelement überlagert wird, z. B. einem auf transparent festgelegten **GroupBox-Steuerelement,** erfasst InkPicture keine InkPicture-Daten. InkPicture muss das oberste Steuerelement in der Z-Reihenfolge oder ein untergeordnetes Steuerelement von **GroupBox sein.**

 

## <a name="com-implementation"></a>COM-Implementierung

Dieses Objekt implementiert die **IInkPicture-COM-Schnittstelle.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[InkEdit-Steuerelementreferenz](inkedit-control-reference.md)
</dt> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> </dl>

