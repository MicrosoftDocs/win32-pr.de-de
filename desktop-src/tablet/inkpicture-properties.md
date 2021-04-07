---
description: Dieser Abschnitt enthält Eigenschaften für das InkPicture-Steuerelement.
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: InkPicture-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ae8149098b34a70af5e088814e2a5258b0fa0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759528"
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
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw (Eigenschaft)</strong></a></td>
<td>Ruft einen Wert ab bzw. legt einen Wert fest, der angibt, ob das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement neu gezeichnet wird, wenn das Fenster ungültig wird (d. h., das <a href="inkdisp-class.md"><strong>InkDisp</strong></a> -Objekt, das momentan WM_PAINT dem InkPicture-Steuerelement zugeordnet ist, wird automatisch neu gezeichnet, wenn das Fenster, das<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></td>
<td>Ruft die Hintergrundfarbe für das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement ab oder legt diese fest. Die Standard Hintergrundfarbe ist die Hintergrundfarbe des System Fensters, die in der Regel weiß ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk (Eigenschaft)</strong></a></td>
<td>Ruft den-Wert ab, der angibt, ob das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement frei Hand Eingaben sammelt (nur Laufzeit).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode '</strong></a></td>
<td>Ruft den Auflistungs Modus ab, der bestimmt, ob Freihand-, Gesten-oder frei Hand Eingaben und Gesten beim Schreiben des Benutzers erkannt werden<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors-Eigenschaft</strong></a></td>
<td>Ruft die <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>iinkcursors</strong></a> -Auflistung ab, die im Freihand-Bereich des <a href="inkpicture-control-reference.md">InkPicture</a> -Steuer Elements verwendet werden können.<br/></td>
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
<td>Ruft die Paketbeschreibung des <a href="inkpicture-control-reference.md">InkPicture</a> -Steuer Elements ab oder legt Sie fest (nur Laufzeit).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering (Eigenschaft)</strong></a></td>
<td>Ruft den-Wert ab oder legt diesen fest, der angibt, ob das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement die frei Handschrift beim Sammeln dynamisch rendert<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></td>
<td>Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob sich das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement im Freihand-, Lösch-oder Bearbeitungsmodus befindet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Aktiviert</strong></a></td>
<td>Ruft einen Wert ab, der bestimmt, ob das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement auf benutzergenerierte Ereignisse reagieren kann, oder legt diesen fest.<br/>
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
<td>Ruft das Fenster Handle ab, an das das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement gebunden ist. (nur Laufzeit)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Freihand</strong></a></td>
<td>Ruft das <a href="inkdisp-class.md"><strong>InkDisp</strong></a> -Objekt ab, das dem <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement zugeordnet ist, oder legt dieses fest (nur Lauf Zeit).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></td>
<td>Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement Stift Eingaben sammelt (in-Air-Pakete, Cursor-in-Range-Ereignisse usw.).<br/></td>
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
<td>Dient zum Abrufen oder Festlegen eines Werts, der den Typ des Mauszeigers angibt, der angezeigt wird, wenn sich der Mauszeiger über einem bestimmten Teil des <a href="inkpicture-control-reference.md">InkPicture</a> -Steuer Elements befindet<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></td>
<td>Ruft die Grafikdatei ab, die im <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement angezeigt werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (Eigenschaft)</strong></a></td>
<td>Ruft das <a href="inkrenderer-class.md"><strong>inkrenderer</strong></a> -Objekt ab, das zum Zeichnen von frei Hand Eingaben im <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement verwendet wird (nur Laufzeit), oder legt dieses fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Auswahl</strong></a></td>
<td>Ruft die aktuell im <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement ausgewählte <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">inkstrokes</a> -Auflistung ab (nur Laufzeit).<br/></td>
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
<td>Ruft das <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>iinktablet</strong></a> -Objekt ab, das das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement zurzeit zum Erfassen von Eingaben verwendet.<br/></td>
</tr>
</tbody>
</table>



 

