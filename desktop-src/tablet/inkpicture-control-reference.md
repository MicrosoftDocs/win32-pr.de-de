---
description: Mit dem InkPicture-Steuerelement können Sie ein Bild in einer Anwendung platzieren und Benutzern das Hinzufügen von frei Hand Eingaben ermöglichen.
ms.assetid: e9fa6807-6e2a-44ec-9b8f-a560185e4367
title: InkPicture-Steuerelement Verweis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8caaf1970394338f858cd0fdff0dab58153f53b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960859"
---
# <a name="inkpicture-control-reference"></a>InkPicture-Steuerelement Verweis

Mit dem InkPicture-Steuerelement können Sie ein Bild in einer Anwendung platzieren und Benutzern das Hinzufügen von frei Hand Eingaben ermöglichen. Es ist für Szenarien vorgesehen, in denen frei Hand Eingaben nicht als Text erkannt werden, sondern stattdessen als frei Hand Eingaben gespeichert werden.

Das InkPicture-Steuerelement kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

> [!Note]  
> Das InkPicture-Steuerelement ist für die Skripterstellung nicht als sicher markiert. Das InkPicture-Steuerelement sollte nicht in HTML-oder ASP.NET-Seiten verwendet werden.

 

Wenn Sie das InkPicture-Steuerelement hinter einem transparenten Steuerelement erstellen (z. b. ein GroupBox-Element mit dem \_ \_ transparenten Eigenschaften Satz von WS-Ex), wird das Sammeln von frei Hand

## <a name="members"></a>Member



| Enumeration                                      | Beschreibung                                                                                              |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Inkpicturesizemode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpicturesizemode) | Definiert Werte, die angeben, wie sich das Hintergrundbild innerhalb des InkPicture-Steuer Elements verhält.<br/> |



 



| Ereignis                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ChangeUICues**                                                                   | Veraltet.<br/>                                                                                                                                                                                                                                                                                             |
| [**Sie**](inkpicture-click.md)                                                  | Tritt auf, wenn ein Benutzer auf das InkPicture-Steuerelement klickt.<br/>                                                                                                                                                                                                                                                       |
| [**Currsorbuttondown-Ereignis**](inkpicture-cursorbuttondown.md)                      | Tritt auf, wenn das [**InkCollector**](inkcollector-class.md) -Steuerelement ein nicht herunter gesteuerbares [**iinkcurrsorbutton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) -Objekt erkennt.<br/>                                                                                                                                                         |
| [**Currsorbuttonup-Ereignis**](inkpicture-cursorbuttonup.md)                          | Tritt auf, wenn das InkPicture-Steuerelement eine [**iinkcursor-Schaltfläche**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) erkennt, die aktiv ist.<br/>                                                                                                                                                                                                  |
| [**Ereignis "Cursor"**](inkpicture-cursordown.md)                                  | Tritt auf, wenn die Cursor-QuickInfo die digitalisierende Tablet-Oberfläche kontaktiert<br/>                                                                                                                                                                                                                                      |
| [**Cursor Event Range-Ereignis**](inkpicture-cursorinrange.md)                            | Tritt auf, wenn ein Cursor in den physischen Erkennungsbereich (Near) des Tablet-Kontexts eintritt.<br/>                                                                                                                                                                                                             |
| [**Cursor-Ereignis**](inkpicture-cursoroutofrange.md)                      | Tritt auf, wenn der Cursor den physischen Erkennungsbereich (Nähe) des Tablet-Kontexts verlässt.<br/>                                                                                                                                                                                                           |
| [**DblClick**](inkpicture-dblclick.md)                                            | Tritt auf, wenn auf das InkPicture-Steuerelement Doppel geklickt wird.<br/> Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert. Die **\_ iinkpictureevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ipedblclick.<br/> |
| [**Gesten Ereignis**](inkpicture-gesture.md)                                        | Tritt auf, wenn eine Anwendungs Geste erkannt wird.<br/>                                                                                                                                                                                                                                                       |
| [**Tastatur Bild-Steuerelement für KeyDown-Ereignis \[\]**](inkpicture-keydown.md)                 | Tritt auf, wenn eine Taste gedrückt wird, während das InkPicture-Steuerelement den Fokus besitzt.<br/>                                                                                                                                                                                                           |
| [**KeyPress-Ereignis \[ inkbild-Steuerelement\]**](inkpicture-keypress.md)                | Tritt auf, wenn eine Taste gedrückt wird, während das InkPicture-Steuerelement den Fokus besitzt.<br/>                                                                                                                                                                                                                                    |
| [**KeyUp-Ereignis \[ inkbild-Steuerelement\]**](inkpicture-keyup.md)                     | Tritt auf, wenn eine Taste losgelassen wird, während das InkPicture-Steuerelement den Fokus besitzt.<br/>                                                                                                                                                                                                                                   |
| [**Mousdown-Ereignis, \[ inkbild-Steuerelement\]**](inkpicture-mousedown.md)             | Tritt ein, wenn sich der Mauszeiger über dem InkPicture-Steuerelement befindet und eine Maustaste gedrückt wird.<br/>                                                                                                                                                                                                             |
| [**MouseEnter**](inkpicture-mouseenter.md)                                        | Tritt ein, wenn der Mauszeiger in das InkPicture-Steuerelement eintritt.<br/>                                                                                                                                                                                                                                            |
| [**Moupagehover**](inkpicture-mousehover.md)                                        | Tritt auf, wenn der Mauszeiger über das InkPicture-Steuerelement bewegt wird.<br/>                                                                                                                                                                                                                                       |
| [**MouseLeave**](inkpicture-mouseleave.md)                                        | Tritt ein, wenn der Mauszeiger das InkPicture-Steuerelement verlässt.<br/>                                                                                                                                                                                                                                            |
| [**Mousmove-Ereignis \[ inkbild-Steuerelement\]**](inkpicture-mousemove.md)             | Tritt ein, wenn der Mauszeiger über das InkPicture-Steuerelement bewegt wird.<br/>                                                                                                                                                                                                                                     |
| [**Mousup-Ereignis \[ inkbild-Steuerelement\]**](inkpicture-mouseup.md)                 | Tritt ein, wenn sich der Mauszeiger über dem InkPicture-Steuerelement befindet und eine Maustaste losgelassen wird.<br/>                                                                                                                                                                                                            |
| [**Mausrad**](inkpicture-mousewheel.md)                                        | Tritt auf, wenn das Mausrad bewegt wird, während das inkbilsteuerelement den Fokus besitzt.<br/>                                                                                                                                                                                                                               |
| [**"Nwinairpakete"-Ereignis**](inkpicture-newinairpackets.md)                        | Tritt auf, wenn ein in-Air-Paket angezeigt wird.<br/>                                                                                                                                                                                                                                                                   |
| [**Newpakete-Ereignis**](inkpicture-newpackets.md)                                  | Tritt auf, wenn das InkPicture-Steuerelement ein Paket empfängt.<br/>                                                                                                                                                                                                                                                   |
| [**Be**](inkpicture-painted.md)                                              | Tritt auf, wenn das InkPicture-Steuerelement das erneute zeichnen selbst abgeschlossen hat.<br/>                                                                                                                                                                                                                                      |
| [**Be**](inkpicture-painting.md)                                            | Tritt ein, bevor das InkPicture-Steuerelement sich selbst neu zeichnet.<br/>                                                                                                                                                                                                                                                    |
| [**Größe ändern**](inkpicture-resize.md)                                                | Tritt ein, wenn die Größe des InkPicture-Steuer Elements geändert wird.<br/>                                                                                                                                                                                                                                                          |
| [**SelectionChanged**](inkpicture-selectionchanged.md)                            | Tritt auf, wenn sich die Auswahl von Text innerhalb des InkPicture-Steuer Elements geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, Ausschneide-und Einfüge Prozeduren oder die [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) -Eigenschaft.<br/>                                                                                    |
| [**Ereignis**](inkpicture-selectionchanging.md)                          | Tritt auf, wenn sich die Auswahl von Text innerhalb des InkPicture-Steuer Elements ändert, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und Einfüge Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) -Eigenschaft.<br/>                                                                             |
| [**Selectionverschoben**](inkpicture-selectionmoved.md)                                | Tritt auf, wenn sich die Position der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) -Eigenschaft.<br/>                                                                                                  |
| [**SelectionMoving-Ereignis, \[ inkbild-Steuerelement\]**](inkpicture-selectionmoving.md) | Tritt ein, wenn die Position der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) -Eigenschaft.<br/>                                                                                           |
| [**SelectionResized**](inkpicture-selectionresized.md)                            | Tritt auf, wenn sich die Größe der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der [**Auswahl**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) Eigenschaft.<br/>                                                                                                      |
| [**Selectionresisierend**](inkpicture-selectionresizing.md)                          | Tritt ein, wenn die Größe der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) -Eigenschaft.<br/>                                                                                               |
| [**SizeChanged**](inkpicture-sizechanged.md)                                      | Tritt auf, nachdem die Größe des InkPicture-Steuer Elements geändert wurde, genauer gesagt, nachdem sich der Wert der [**Breite**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) oder [**Höhe**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) geändert hat.<br/>                                                                                                      |
| [**SizeModeChanged**](inkpicture-sizemodechanged.md)                              | Tritt auf, nachdem die [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) -Eigenschaft des InkPicture-Steuer Elements geändert wurde.<br/>                                                                                                                                                                                           |
| **StyleChanged**                                                                   | Nicht implementiert.<br/>                                                                                                                                                                                                                                                                                        |
| [**Stellung**](inkpicture-stroke.md)                                                | Tritt ein, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.<br/>                                                                                                                                                                                                                                                  |
| [**StrokesDeleted**](inkpicture-strokesdeleted.md)                                | Tritt auf, nachdem [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte aus der [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) -Eigenschaft gelöscht wurden.<br/>                                                                                                                                                                        |
| [**Strokeslöschung**](inkpicture-strokesdeleting.md)                              | Tritt auf, bevor [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte aus der [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) -Eigenschaft gelöscht werden.<br/>                                                                                                                                                                             |
| [**Systemcolorschge**](inkpicture-systemcolorschanged.md)                      | Tritt ein, nachdem sich die Systemfarben geändert haben.<br/>                                                                                                                                                                                                                                                                  |
| [**System Bewegung**](inkpicture-systemgesture.md)                                  | Tritt auf, wenn eine System Bewegung erkannt wird.<br/>                                                                                                                                                                                                                                                             |
| [**TabletAdded-Ereignis**](inkpicture-tabletadded.md)                                | Tritt auf, wenn dem System ein Tablet hinzugefügt wird.<br/>                                                                                                                                                                                                                                                            |
| [**Tabletreverschodas Ereignis**](inkpicture-tabletremoved.md)                            | Tritt auf, wenn ein Tablet aus dem System entfernt wird.<br/>                                                                                                                                                                                                                                                        |



 



| Methode                                                                                   | BESCHREIBUNG                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Geteventinterest-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | Gibt einen Wert zurück, der angibt, ob das InkPicture-Steuerelement an einem bestimmten Ereignis interessiert ist.<br/>                                                                   |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | Gibt einen Wert zurück, der angibt, ob das InkPicture-Steuerelement an einer bestimmten Anwendungs Geste interessiert ist.<br/>                                                     |
| [**Getwindowinputrechteck-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | Gibt das Fenster Rechteck in Pixel zurück, in dem frei Hand Eingaben gezeichnet werden.<br/>                                                                                                 |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | Gibt einen Member der [**SelectionHitResult**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) -Enumeration zurück, der angibt, welcher Teil einer Auswahl, falls vorhanden, während eines Treffer Tests getroffen wurde.<br/> |
| [**Setalltablezmode-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | Ermöglicht dem InkPicture-Steuerelement, frei Hand Eingaben von jedem Tablet zu erfassen, das an den Tablet PC angeschlossen ist<br/>                                                                            |
| [**""-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | Legt einen Wert fest, der angibt, ob ein InkPicture-Steuerelement an einem angegebenen Ereignis interessiert ist.<br/>                                                                        |
| SetFocus                                                                                 | Verschiebt den Fokus auf das InkPicture-Steuerelement.<br/>                                                                                                                          |
| [**SetGestureStatus-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | Legt das Interesse des InkPicture-Objekts in einer angegebenen Anwendungs Geste fest.<br/>                                                                                      |
| [**SetSingleTabletIntegratedMode-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | Legt fest, dass das InkPicture-Steuerelement Freihand von nur einem Tablet sammelt, das an den Tablet PC angeschlossen ist Frei Hand Eingaben von anderen Tablets werden ignoriert.<br/>                                       |
| [**Setwindowinputrechteck-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | Gibt das Fenster Rechteck an, das in Fenster Koordinaten festgelegt werden soll, in dem frei Hand Eingaben gezeichnet werden.<br/>                                                                            |
| ShowWhatsThis                                                                            | Zeigt ein ausgewähltes Thema in einer Hilfedatei mithilfe des Popups "What es this" an, das von der Hilfe in 32-Bit-Microsoft Windows-Betriebssystemen bereitgestellt wird (nur zur Entwurfszeit).<br/>           |
| ZOrder                                                                                   | Platziert das Steuerelement an der Vorder-oder Rückseite der z-Reihenfolge innerhalb der grafischen Ebene (nur zur Entwurfszeit).<br/>                                                               |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw (Eigenschaft)</strong></a></td>
<td>Ruft einen Wert ab bzw. legt einen Wert fest, der angibt, ob das InkPicture-Steuerelement neu gezeichnet wird, wenn das Fenster ungültig wird (d. h., das <a href="inkdisp-class.md"><strong>InkDisp</strong></a> -Objekt, das momentan WM_PAINT dem InkPicture-Steuerelement zugeordnet ist, wird automatisch neu gezeichnet, wenn das Fenster, das<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></td>
<td>Ruft die Hintergrundfarbe für das InkPicture-Steuerelement ab oder legt diese fest. Die Standard Hintergrundfarbe ist die Hintergrundfarbe des System Fensters, die in der Regel weiß ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk (Eigenschaft)</strong></a></td>
<td>Ruft den-Wert ab, der angibt, ob das InkPicture-Steuerelement frei Hand Eingaben sammelt (nur Laufzeit).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode '</strong></a></td>
<td>Ruft den Auflistungs Modus ab, der bestimmt, ob Freihand-, Gesten-oder frei Hand Eingaben und Gesten beim Schreiben des Benutzers erkannt werden<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors-Eigenschaft</strong></a></td>
<td>Ruft die <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>iinkcursors</strong></a> -Auflistung ab, die im Freihand-Bereich des InkPicture-Steuer Elements verwendet werden können.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></td>
<td>Ruft die <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>iinkcustomstrokes</strong></a> -Auflistung ab, die mit der frei Hand Eingabe beibehalten werden soll (nur zur Entwurfszeit).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes (Eigenschaft)</strong></a></td>
<td>Ruft die standardmäßige <a href="inkdrawingattributes-class.md"><strong>inkdrawingattributes</strong></a> -Auflistung ab, die beim Zeichnen und Anzeigen von frei Hand Eingaben verwendet werden soll (nur Laufzeit)<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription (Eigenschaft)</strong></a></td>
<td>Ruft die Paketbeschreibung des InkPicture-Steuer Elements ab oder legt Sie fest (nur Laufzeit).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering (Eigenschaft)</strong></a></td>
<td>Ruft den-Wert ab oder legt diesen fest, der angibt, ob das InkPicture-Steuerelement die frei Handschrift beim Sammeln dynamisch rendert<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></td>
<td>Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob sich das InkPicture-Steuerelement im Freihand-, Lösch-oder Bearbeitungsmodus befindet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Aktiviert</strong></a></td>
<td>Ruft einen Wert ab, der bestimmt, ob das InkPicture-Steuerelement auf benutzergenerierte Ereignisse reagieren kann, oder legt diesen fest.<br/>
<blockquote>
[!Note]<br />
Diese Eigenschaft entspricht der <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> -Eigenschaft.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></td>
<td>Ruft den-Wert ab, der angibt, ob frei Hand Eingaben durch Strich oder Punkt gelöscht werden, oder legt ihn fest<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></td>
<td>Ruft den-Wert ab, der die Breite des Radierers für Stift Tipps angibt, oder legt diesen fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>HWND</strong></a></td>
<td>Ruft das Fenster Handle ab, an das das InkPicture-Steuerelement gebunden ist. (nur Laufzeit)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Freihand</strong></a></td>
<td>Ruft das <a href="inkdisp-class.md"><strong>InkDisp</strong></a> -Objekt ab, das dem InkPicture-Steuerelement zugeordnet ist, oder legt dieses fest (nur Lauf Zeit).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></td>
<td>Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob das InkPicture-Steuerelement Stift Eingaben sammelt (in-Air-Pakete, Cursor-in-Range-Ereignisse usw.).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX (Eigenschaft)</strong></a></td>
<td>Ruft den x-Achsen Rand um das Fenster Rechteck in Bildschirm Koordinaten ab oder legt diesen fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY-Eigenschaft</strong></a></td>
<td>Ruft den y-Achsen Rand um das Fenster Rechteck in Bildschirm Koordinaten ab oder legt diesen fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon-Eigenschaft</strong></a></td>
<td>Ruft das aktuelle benutzerdefinierte Maus Symbol ab oder legt es fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>Mougenpointer (Eigenschaft)</strong></a></td>
<td>Dient zum Abrufen oder Festlegen eines Werts, der den Typ des Mauszeigers angibt, der angezeigt wird, wenn sich der Mauszeiger über einem bestimmten Teil des InkPicture-Steuer Elements befindet<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></td>
<td>Ruft die Grafikdatei ab, die im InkPicture-Steuerelement angezeigt werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (Eigenschaft)</strong></a></td>
<td>Ruft das <a href="inkrenderer-class.md"><strong>inkrenderer</strong></a> -Objekt ab, das zum Zeichnen von frei Hand Eingaben im InkPicture-Steuerelement verwendet wird (nur Laufzeit), oder legt dieses fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Auswahl</strong></a></td>
<td>Ruft die aktuell im InkPicture-Steuerelement ausgewählte <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">inkstrokes</a> -Auflistung ab (nur Laufzeit).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>Größenanpassung</strong></a></td>
<td>Ruft ab oder legt fest, wie das Steuerelement Bild Platzierung und Größenanpassung behandelt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk (Eigenschaft)</strong></a></td>
<td>Ruft einen Wert ab, der angibt, ob frei Hand Eingaben als nur eine Farbe, Color = COLOR_WINDOWTEXT (aus dem GetSystemMetrics-Befehl) gerendert werden, wenn sich das System im hoher Kontrast Modus befindet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></td>
<td>Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob alle Benutzeroberflächen für die Auswahl (Begrenzungs-und Auswahl Handles) im hohen Kontrast gezeichnet werden, wenn sich das System im hoher Kontrast Modus befindet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Tablet-Eigenschaft</strong></a></td>
<td>Ruft das <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>iinktablet</strong></a> -Objekt ab, das das InkPicture-Steuerelement zurzeit zum Erfassen von Eingaben verwendet.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Die Laufzeit-Benutzeroberfläche für das InkPicture-Steuerelement ist ein Fenster mit einem nicht transparenten Hintergrund (einzelne Farbe, Bild Hintergrund oder beides), das nicht transparente Freihand enthält.

Sie können das InkPicture-Steuerelement verwenden, um frei Hand Eingaben in Microsoft Windows 2000, Windows Server 2003, jeder anderen Edition von Windows XP als Windows XP Tablet PC Edition und allen Versionen von Windows Vista zu ermöglichen. Sie können jedoch nur unter den folgenden Bedingungen frei Hand Eingaben, Gesten akzeptieren oder Handschrift erkennen:

-   Frei Hand Eingaben können eingegeben und erkannt werden, wenn Windows Vista oder XP Tablet PC Edition 2005 installiert ist.
-   Gesten können ebenfalls erkannt werden.
-   Handschrift kann als Text erkannt werden, wenn die Handschrift von Computern stammt, auf denen ältere Versionen von Windows ausgeführt werden, solange Erkennungsgeräte vorhanden sind.

Wenn Sie Windows 2000, Windows Server 2003, eine beliebige andere Edition von Windows XP als Windows XP Tablet PC Edition 2005 verwenden, können Sie den Umgebungs Eigenschaften des InkPicture-Steuer Elements Werte zuweisen und dann frei Hand Eingaben in andere Anwendungen kopieren und einfügen. Der Wert der InkEnabled-Eigenschaft ist jedoch immer **false**.

Persistente [**InkDisp**](inkdisp-class.md) -Objekte können in allen Editionen von Windows Vista und XP und auf Systemen, auf denen nur das Windows XP Tablet PC Edition Software Development Kit (SDK) installiert ist, geladen und angezeigt werden. **InkDisp** -Objekte können nur in Text (erkannt) konvertiert werden, wenn Windows Vista oder Windows XP Tablet PC Edition 2005 installiert ist.

Wenn Vorgänge für dieses Steuerelement nicht erfolgreich sind, wird ein zulässiges HRESULT zurückgegeben. Wenn Fehlerbedingungen auftreten, überprüfen Sie das zurückgegebene HRESULT auf den Fehler.

Weitere Informationen zu frei Hand Steuerelementen finden Sie unter [Ink](ink-controls.md).

Informationen dazu, welche Threads bestimmte Ereignisse auslösen, finden Sie unter [Threads, auf die ein Ereignis](threads-on-which-an-event-can-fire.md)ausgelöst werden kann.

Um die Leistung Ihrer Anwendung zu verbessern, löschen Sie ein InkPicture-Steuerelement manuell, wenn es nicht mehr benötigt wird.

> [!Note]  
> Wenn ein InkPicture-Steuerelement mit einem anderen Steuerelement überlastet wird, z. b. ein auf transparent festgelegtes **GroupBox** -Element, sammelt InkPicture keine Freihand. Das InkPicture muss das oberste Steuerelement in der Z-Reihenfolge sein, oder es muss ein untergeordnetes Element der **GroupBox** sein.

 

## <a name="com-implementation"></a>COM-Implementierung

Dieses Objekt implementiert die **iinkpicture** -com-Schnittstelle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zum InkEdit-Steuerelement](inkedit-control-reference.md)
</dt> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> </dl>

