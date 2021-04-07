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
# <a name="inkpicture-properties"></a><span data-ttu-id="85c90-103">InkPicture-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85c90-103">InkPicture Properties</span></span>

<span data-ttu-id="85c90-104">Dieser Abschnitt enthält Eigenschaften für das InkPicture-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="85c90-104">This section contains Properties for the InkPicture Control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85c90-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="85c90-105">Property</span></span></th>
<th><span data-ttu-id="85c90-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85c90-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85c90-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw (Eigenschaft)</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-108">Ruft einen Wert ab bzw. legt einen Wert fest, der angibt, ob das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement neu gezeichnet wird, wenn das Fenster ungültig wird (d. h., das <a href="inkdisp-class.md"><strong>InkDisp</strong></a> -Objekt, das momentan WM_PAINT dem InkPicture-Steuerelement zugeordnet ist, wird automatisch neu gezeichnet, wenn das Fenster, das</span><span class="sxs-lookup"><span data-stu-id="85c90-108">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control repaints when the window is invalidated (whether the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object currently associated with InkPicture control is automatically redrawn when the window associated with the InkPicture receives a WM_PAINT message).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></span></span></td>
<td><span data-ttu-id="85c90-110">Ruft die Hintergrundfarbe für das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="85c90-110">Gets or sets the background color for the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span> <span data-ttu-id="85c90-111">Die Standard Hintergrundfarbe ist die Hintergrundfarbe des System Fensters, die in der Regel weiß ist.</span><span class="sxs-lookup"><span data-stu-id="85c90-111">The default background color is the system window background color, which is typically white.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk (Eigenschaft)</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-113">Ruft den-Wert ab, der angibt, ob das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement frei Hand Eingaben sammelt (nur Laufzeit).</span><span class="sxs-lookup"><span data-stu-id="85c90-113">Gets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is collecting ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode '</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></span></span></td>
<td><span data-ttu-id="85c90-115">Ruft den Auflistungs Modus ab, der bestimmt, ob Freihand-, Gesten-oder frei Hand Eingaben und Gesten beim Schreiben des Benutzers erkannt werden</span><span class="sxs-lookup"><span data-stu-id="85c90-115">Gets or sets the collection mode that determines whether ink, gestures, or ink and gestures are recognized as the user writes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors-Eigenschaft</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-117">Ruft die <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>iinkcursors</strong></a> -Auflistung ab, die im Freihand-Bereich des <a href="inkpicture-control-reference.md">InkPicture</a> -Steuer Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="85c90-117">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> collection available for use in the <a href="inkpicture-control-reference.md">InkPicture</a> control's inking region.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span></span></td>
<td><span data-ttu-id="85c90-119">Ruft die <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>iinkcustomstrokes</strong></a> -Auflistung ab, die mit der frei Hand Eingabe beibehalten werden soll (nur zur Entwurfszeit).</span><span class="sxs-lookup"><span data-stu-id="85c90-119">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> collection to be persisted with the ink (design-time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes (Eigenschaft)</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-121">Ruft die standardmäßige <a href="inkdrawingattributes-class.md"><strong>inkdrawingattributes</strong></a> -Auflistung ab, die beim Zeichnen und Anzeigen von frei Hand Eingaben verwendet werden soll (nur Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="85c90-121">Gets or sets the default <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> collection to use when drawing and displaying ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription (Eigenschaft)</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-123">Ruft die Paketbeschreibung des <a href="inkpicture-control-reference.md">InkPicture</a> -Steuer Elements ab oder legt Sie fest (nur Laufzeit).</span><span class="sxs-lookup"><span data-stu-id="85c90-123">Gets or sets the packet description of the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering (Eigenschaft)</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-125">Ruft den-Wert ab oder legt diesen fest, der angibt, ob das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement die frei Handschrift beim Sammeln dynamisch rendert</span><span class="sxs-lookup"><span data-stu-id="85c90-125">Gets or sets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control dynamically renders the ink as it is collected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span></span></td>
<td><span data-ttu-id="85c90-127">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob sich das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement im Freihand-, Lösch-oder Bearbeitungsmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="85c90-127">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is in ink mode, deletion mode, or selecting/editing mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Aktiviert</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Enabled</strong></a></span></span></td>
<td><span data-ttu-id="85c90-129">Ruft einen Wert ab, der bestimmt, ob das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement auf benutzergenerierte Ereignisse reagieren kann, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="85c90-129">Gets or sets a value that determines whether the <a href="inkpicture-control-reference.md">InkPicture</a> control can respond to user-generated events.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="85c90-130">Diese Eigenschaft entspricht der <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="85c90-130">This property is equivalent to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> property.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span></span></td>
<td><span data-ttu-id="85c90-132">Ruft den-Wert ab, der angibt, ob frei Hand Eingaben durch Strich oder Punkt gelöscht werden, oder legt ihn fest</span><span class="sxs-lookup"><span data-stu-id="85c90-132">Gets or sets the value that specifies whether ink is erased by stroke or by point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span></span></td>
<td><span data-ttu-id="85c90-134">Ruft den-Wert ab, der die Breite des Radierers für Stift Tipps angibt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="85c90-134">Gets or sets the value that specifies the width of the eraser pen tip.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>HWND</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></span></span></td>
<td><span data-ttu-id="85c90-136">Ruft das Fenster Handle ab, an das das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="85c90-136">Gets the window handle to which the <a href="inkpicture-control-reference.md">InkPicture</a> control is bound.</span></span> <span data-ttu-id="85c90-137">(nur Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="85c90-137">(run time only)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Freihand</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Ink</strong></a></span></span></td>
<td><span data-ttu-id="85c90-139">Ruft das <a href="inkdisp-class.md"><strong>InkDisp</strong></a> -Objekt ab, das dem <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement zugeordnet ist, oder legt dieses fest (nur Lauf Zeit).</span><span class="sxs-lookup"><span data-stu-id="85c90-139">Gets or sets the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object that is associated with the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span></span></td>
<td><span data-ttu-id="85c90-141">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement Stift Eingaben sammelt (in-Air-Pakete, Cursor-in-Range-Ereignisse usw.).</span><span class="sxs-lookup"><span data-stu-id="85c90-141">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control collects pen input (in-air packets, cursor in range events, and so on).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX (Eigenschaft)</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-143">Ruft den x-Achsen Rand um das Fenster Rechteck in Bildschirm Koordinaten ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="85c90-143">Gets or sets the x-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY-Eigenschaft</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-145">Ruft den y-Achsen Rand um das Fenster Rechteck in Bildschirm Koordinaten ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="85c90-145">Gets or sets the y-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon-Eigenschaft</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-147">Ruft das aktuelle benutzerdefinierte Maus Symbol ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="85c90-147">Gets or sets the current custom mouse icon.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>Mougenpointer (Eigenschaft)</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-149">Dient zum Abrufen oder Festlegen eines Werts, der den Typ des Mauszeigers angibt, der angezeigt wird, wenn sich der Mauszeiger über einem bestimmten Teil des <a href="inkpicture-control-reference.md">InkPicture</a> -Steuer Elements befindet</span><span class="sxs-lookup"><span data-stu-id="85c90-149">Gets or sets a value that indicates the type of mouse pointer that appears when the mouse is over a particular part of the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></span></span></td>
<td><span data-ttu-id="85c90-151">Ruft die Grafikdatei ab, die im <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="85c90-151">Gets the graphics file to appear on the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (Eigenschaft)</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-153">Ruft das <a href="inkrenderer-class.md"><strong>inkrenderer</strong></a> -Objekt ab, das zum Zeichnen von frei Hand Eingaben im <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement verwendet wird (nur Laufzeit), oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="85c90-153">Gets or sets the <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> object that is used to draw ink on the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Auswahl</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selection</strong></a></span></span></td>
<td><span data-ttu-id="85c90-155">Ruft die aktuell im <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement ausgewählte <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">inkstrokes</a> -Auflistung ab (nur Laufzeit).</span><span class="sxs-lookup"><span data-stu-id="85c90-155">Gets the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection currently selected inside the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>Größenanpassung</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span></span></td>
<td><span data-ttu-id="85c90-157">Ruft ab oder legt fest, wie das Steuerelement Bild Platzierung und Größenanpassung behandelt.</span><span class="sxs-lookup"><span data-stu-id="85c90-157">Gets or sets how the control handles image placement and sizing.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk (Eigenschaft)</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-159">Ruft einen Wert ab, der angibt, ob frei Hand Eingaben als nur eine Farbe, Color = COLOR_WINDOWTEXT (aus dem GetSystemMetrics-Befehl) gerendert werden, wenn sich das System im hoher Kontrast Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="85c90-159">Gets a value that specifies whether ink is rendered as just one color, Color = COLOR_WINDOWTEXT (from the GetSystemMetrics call) when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85c90-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span></span></td>
<td><span data-ttu-id="85c90-161">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob alle Benutzeroberflächen für die Auswahl (Begrenzungs-und Auswahl Handles) im hohen Kontrast gezeichnet werden, wenn sich das System im hoher Kontrast Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="85c90-161">Gets or sets a value that specifies whether all selection user interfaces (selection bounding box and selection handles) are drawn in high contrast when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85c90-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Tablet-Eigenschaft</strong></a></span><span class="sxs-lookup"><span data-stu-id="85c90-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Tablet Property</strong></a></span></span></td>
<td><span data-ttu-id="85c90-163">Ruft das <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>iinktablet</strong></a> -Objekt ab, das das <a href="inkpicture-control-reference.md">InkPicture</a> -Steuerelement zurzeit zum Erfassen von Eingaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="85c90-163">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> object that the <a href="inkpicture-control-reference.md">InkPicture</a> control is currently using to collect input.</span></span><br/></td>
</tr>
</tbody>
</table>



 

