---
description: Dieser Abschnitt enthält Eigenschaften für das InkPicture-Steuerelement.
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: InkPicture-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359626adecfa9ea7eb7c60ae58754f2e544b6ca8db3bf362ddfb83af49cd5ff3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712510"
---
# <a name="inkpicture-properties"></a>InkPicture-Eigenschaften

Dieser Abschnitt enthält Eigenschaften für das InkPicture-Steuerelement.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw-Eigenschaft</strong></a></td>
<td>Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob das <a href="inkpicture-control-reference.md">InkPicture-Steuerelement</a> neu zeichnet, wenn das Fenster ungültig wird (ob das derzeit dem InkPicture-Steuerelement zugeordnete <a href="inkdisp-class.md"><strong>InkDisp-Objekt</strong></a> automatisch neu gezeichnet wird, wenn das der InkPicture zugeordnete Fenster eine WM_PAINT Meldung empfängt).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>Backcolor</strong></a></td>
<td>Ruft die Hintergrundfarbe für das <a href="inkpicture-control-reference.md">InkPicture-Steuerelement</a> ab oder legt diese fest. Die Standardhintergrundfarbe ist die Hintergrundfarbe des Systemfensters, die in der Regel weiß ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk-Eigenschaft</strong></a></td>
<td>Ruft den Wert ab, der angibt, ob das <a href="inkpicture-control-reference.md">InkPicture-Steuerelement</a> inkk erfasst (nur Laufzeit).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></td>
<td>Ruft den Auflistungsmodus ab, der bestimmt, ob Ink, Gesten oder Ink und Gesten beim Schreiben des Benutzers erkannt werden, oder legt diesen fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors-Eigenschaft</strong></a></td>
<td>Ruft die <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors-Auflistung</strong></a> ab, die für die Verwendung im Freihandbereich des <a href="inkpicture-control-reference.md">InkPicture-Steuerelements</a> verfügbar ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>Customstrokes</strong></a></td>
<td>Ruft die <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes-Auflistung</strong></a> ab, die mit der Freihandeingabe beibehalten werden soll (nur zur Entwurfszeit).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes-Eigenschaft</strong></a></td>
<td>Ruft die Standardmäßige <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes-Auflistung</strong></a> ab, die beim Zeichnen und Anzeigen von Ink verwendet werden soll (nur laufzeit).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription-Eigenschaft</strong></a></td>
<td>Ruft die Paketbeschreibung des <a href="inkpicture-control-reference.md">InkPicture-Steuerelements</a> ab (nur Laufzeit) oder legt diese fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering-Eigenschaft</strong></a></td>
<td>Ruft den Wert ab, der angibt, ob das <a href="inkpicture-control-reference.md">InkPicture-Steuerelement die InkPicture-Steuerelement</a> dynamisch rendert, während sie gesammelt wird, oder legt diesen fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>Editingmode</strong></a></td>
<td>Ruft einen Wert ab, der angibt, ob sich das <a href="inkpicture-control-reference.md">InkPicture-Steuerelement</a> im Inkk-Modus, im Löschmodus oder im Auswahl-/Bearbeitungsmodus befindet, oder legt diesen fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Aktiviert</strong></a></td>
<td>Ruft einen Wert ab, der bestimmt, ob das <a href="inkpicture-control-reference.md">InkPicture-Steuerelement</a> auf vom Benutzer generierte Ereignisse reagieren kann, oder legt diesen fest.<br/>
<blockquote>
[!Note]<br />
Diese Eigenschaft entspricht der <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled-Eigenschaft.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></td>
<td>Ruft den Wert ab, der angibt, ob Ink durch Strich oder Punkt gelöscht wird, oder legt diesen fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></td>
<td>Ruft den Wert ab, der die Breite der Radiererstiftspitze angibt, oder legt diesen fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>Hwnd</strong></a></td>
<td>Ruft das Fensterhandle ab, an das das <a href="inkpicture-control-reference.md">InkPicture-Steuerelement</a> gebunden ist. (nur Laufzeit)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Freihand</strong></a></td>
<td>Ruft das <a href="inkdisp-class.md"><strong>InkDisp-Objekt</strong></a> ab, das dem <a href="inkpicture-control-reference.md">InkPicture-Steuerelement</a> zugeordnet ist (nur Laufzeit), oder legt es fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>Inkenabled</strong></a></td>
<td>Ruft einen Wert ab, der angibt, ob das <a href="inkpicture-control-reference.md">InkPicture-Steuerelement</a> Stifteingaben sammelt (In-Air-Pakete, Cursor in Bereichsereignissen usw.), oder legt diesen fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX-Eigenschaft</strong></a></td>
<td>Ruft den X-Achsenrand um das Fensterrechteck in Bildschirmkoordinaten ab oder legt den Rand fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY-Eigenschaft</strong></a></td>
<td>Ruft den Rand der y-Achse um das Fensterrechteck in Bildschirmkoordinaten ab oder legt den Rand fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon-Eigenschaft</strong></a></td>
<td>Ruft das aktuelle benutzerdefinierte Maussymbol ab oder legt dieses fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer-Eigenschaft</strong></a></td>
<td>Ruft einen Wert ab, der den Typ des Mauszeigers angibt, der angezeigt wird, wenn sich die Maus über einem bestimmten Teil des <a href="inkpicture-control-reference.md">InkPicture-Steuerelements</a> befindet, oder legt diesen fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Bild</strong></a></td>
<td>Ruft die Grafikdatei ab, die im <a href="inkpicture-control-reference.md">InkPicture-Steuerelement</a> angezeigt werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderereigenschaft</strong></a></td>
<td>Ruft das <a href="inkrenderer-class.md"><strong>InkRenderer-Objekt</strong></a> ab, das zum Zeichnen von <a href="inkpicture-control-reference.md">InkPicture-Steuerelementen</a> verwendet wird (nur Laufzeit) oder legt dieses fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Auswahl</strong></a></td>
<td>Ruft die <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">Auflistung "InkStrokes"</a> ab, die derzeit im <a href="inkpicture-control-reference.md">InkPicture-Steuerelement</a> ausgewählt ist (nur Laufzeit).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>Größenanpassung</strong></a></td>
<td>Ruft ab oder legt fest, wie das Steuerelement die Bildplatzierung und -dimensionierung behandelt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk-Eigenschaft</strong></a></td>
<td>Ruft einen Wert ab, der angibt, ob Ink als nur eine Farbe gerendert wird, Color = COLOR_WINDOWTEXT (aus dem GetSystemMetrics-Aufruf), wenn sich das System im hoher Kontrast Modus befindet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></td>
<td>Ruft einen Wert ab, der angibt, ob alle Auswahlbenutzeroberflächen (Auswahlgrenzenfeld und Auswahlhandles) in hohem Kontrast gezeichnet werden, wenn sich das System im hoher Kontrast Modus befindet, oder legt diesen fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Tablet-Eigenschaft</strong></a></td>
<td>Ruft das <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet-Objekt</strong></a> ab, das das <a href="inkpicture-control-reference.md">InkPicture-Steuerelement</a> derzeit zum Erfassen von Eingaben verwendet.<br/></td>
</tr>
</tbody>
</table>



 

