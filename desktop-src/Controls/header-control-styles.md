---
title: Header Steuerelement Stile (kommctrl. h)
description: Header Steuerelemente haben einige Stile, die in diesem Abschnitt beschrieben werden, um die Darstellung und das Verhalten des Steuer Elements zu bestimmen. Sie legen die anfänglichen Stile fest, wenn Sie das Header Steuerelement erstellen.
ms.assetid: e47dc6c3-a1af-456c-9235-29ce63f1e13b
topic_type:
- apiref
api_name:
- HDS_BUTTONS
- HDS_DRAGDROP
- HDS_FILTERBAR
- HDS_FLAT
- HDS_FULLDRAG
- HDS_HIDDEN
- HDS_HORZ
- HDS_HOTTRACK
- HDS_CHECKBOXES
- HDS_NOSIZING
- HDS_OVERFLOW
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8450ad39cdb965e3e4be15f0093ec4737a87c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369661"
---
# <a name="header-control-styles"></a><span data-ttu-id="5ce48-104">Header Steuerelement Stile</span><span class="sxs-lookup"><span data-stu-id="5ce48-104">Header Control Styles</span></span>

<span data-ttu-id="5ce48-105">Header Steuerelemente haben einige Stile, die in diesem Abschnitt beschrieben werden, um die Darstellung und das Verhalten des Steuer Elements zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="5ce48-105">Header controls have a number of styles, described in this section, that determine the control's appearance and behavior.</span></span> <span data-ttu-id="5ce48-106">Sie legen die anfänglichen Stile fest, wenn Sie das Header Steuerelement erstellen.</span><span class="sxs-lookup"><span data-stu-id="5ce48-106">You set the initial styles when you create the header control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="5ce48-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="5ce48-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="5ce48-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ce48-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <span data-ttu-id="5ce48-109"><dt><strong>HDS_BUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5ce48-109"><dt><strong>HDS_BUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5ce48-110">Jedes Element im-Steuerelement sieht und verhält sich wie eine Schaltfläche "Push".</span><span class="sxs-lookup"><span data-stu-id="5ce48-110">Each item in the control looks and behaves like a push button.</span></span> <span data-ttu-id="5ce48-111">Dieser Stil ist nützlich, wenn eine Anwendung eine Aufgabe ausführt, wenn der Benutzer auf ein Element im Header Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="5ce48-111">This style is useful if an application carries out a task when the user clicks an item in the header control.</span></span> <span data-ttu-id="5ce48-112">Beispielsweise könnte eine Anwendung Informationen in den Spalten unterschiedlich sortieren, je nachdem, auf welches Element der Benutzer klickt.</span><span class="sxs-lookup"><span data-stu-id="5ce48-112">For example, an application could sort information in the columns differently depending on which item the user clicks.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <span data-ttu-id="5ce48-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5ce48-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5ce48-114">Ermöglicht die Neuanordnung von Header Elementen per Drag & Drop.</span><span class="sxs-lookup"><span data-stu-id="5ce48-114">Allows drag-and-drop reordering of header items.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <span data-ttu-id="5ce48-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5ce48-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5ce48-116">Fügen Sie eine Filter Leiste als Teil des Standard Header-Steuer Elements ein.</span><span class="sxs-lookup"><span data-stu-id="5ce48-116">Include a filter bar as part of the standard header control.</span></span> <span data-ttu-id="5ce48-117">In dieser Leiste können Benutzer bequem einen Filter auf die Anzeige anwenden.</span><span class="sxs-lookup"><span data-stu-id="5ce48-117">This bar allows users to conveniently apply a filter to the display.</span></span> <span data-ttu-id="5ce48-118">Aufrufe an <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> ergeben eine neue Größe für das Steuerelement und bewirken, dass die Listenansicht aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="5ce48-118">Calls to <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> will yield a new size for the control and cause the list view to update.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <span data-ttu-id="5ce48-119"><dt><strong>HDS_FLAT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5ce48-119"><dt><strong>HDS_FLAT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5ce48-120"><a href="common-control-versions.md">Version 6,0 und</a>höher.</span><span class="sxs-lookup"><span data-stu-id="5ce48-120"><a href="common-control-versions.md">Version 6.0 and later</a>.</span></span> <span data-ttu-id="5ce48-121">Bewirkt, dass das Header Steuerelement flach gezeichnet wird, wenn das Betriebssystem im klassischen Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ce48-121">Causes the header control to be drawn flat when the operating system is running in classic mode.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5ce48-122">Comctl32.dll Version 6 ist nicht Verteil Bar, aber Sie ist in Windows enthalten.</span><span class="sxs-lookup"><span data-stu-id="5ce48-122">Comctl32.dll version 6 is not redistributable but it is included in Windows.</span></span> <span data-ttu-id="5ce48-123">Wenn Sie Comctl32.dll Version 6 verwenden möchten, geben Sie ihn in einem Manifest an.</span><span class="sxs-lookup"><span data-stu-id="5ce48-123">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="5ce48-124">Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen</a>.</span><span class="sxs-lookup"><span data-stu-id="5ce48-124">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <span data-ttu-id="5ce48-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5ce48-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5ce48-126">Bewirkt, dass das Header Steuerelement auch dann Spalten Inhalte anzeigt, wenn der Benutzer die Größe einer Spalte ändert.</span><span class="sxs-lookup"><span data-stu-id="5ce48-126">Causes the header control to display column contents even while the user resizes a column.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <span data-ttu-id="5ce48-127"><dt><strong>HDS_HIDDEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5ce48-127"><dt><strong>HDS_HIDDEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5ce48-128">Gibt ein Header Steuerelement an, das ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ce48-128">Indicates a header control that is intended to be hidden.</span></span> <span data-ttu-id="5ce48-129">In diesem Stil wird das Steuerelement nicht ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="5ce48-129">This style does not hide the control.</span></span> <span data-ttu-id="5ce48-130">Wenn Sie die <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> Nachricht stattdessen an ein Header Steuerelement mit dem HDS_HIDDEN Format senden, gibt das Steuerelement im <strong>CY</strong> -Element der <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>Windows</strong></a> -Struktur 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="5ce48-130">Instead, when you send the <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> message to a header control with the HDS_HIDDEN style, the control returns zero in the <strong>cy</strong> member of the <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> structure.</span></span> <span data-ttu-id="5ce48-131">Anschließend blenden Sie das Steuerelement aus, indem Sie die Höhe auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="5ce48-131">You would then hide the control by setting its height to zero.</span></span> <span data-ttu-id="5ce48-132">Dies kann hilfreich sein, wenn Sie das-Steuerelement als Informationscontainer anstelle eines visuellen Steuer Elements verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="5ce48-132">This can be useful when you want to use the control as an information container instead of a visual control.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <span data-ttu-id="5ce48-133"><dt><strong>HDS_HORZ</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5ce48-133"><dt><strong>HDS_HORZ</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5ce48-134">Erstellt ein Header Steuerelement mit horizontaler Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="5ce48-134">Creates a header control with a horizontal orientation.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <span data-ttu-id="5ce48-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5ce48-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5ce48-136">Aktiviert die Hot-Nachverfolgung.</span><span class="sxs-lookup"><span data-stu-id="5ce48-136">Enables hot tracking.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <span data-ttu-id="5ce48-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5ce48-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5ce48-138"><a href="common-control-versions.md">Version 6,00 und</a>höher.</span><span class="sxs-lookup"><span data-stu-id="5ce48-138"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="5ce48-139">Ermöglicht das Platzieren von Kontrollkästchen für Header Elemente.</span><span class="sxs-lookup"><span data-stu-id="5ce48-139">Allows the placing of checkboxes on header items.</span></span> <span data-ttu-id="5ce48-140">Weitere Informationen finden Sie unter dem <strong>fmt</strong> -Member von <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5ce48-140">For more information, see the <strong>fmt</strong> member of <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <span data-ttu-id="5ce48-141"><dt><strong>HDS_NOSIZING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5ce48-141"><dt><strong>HDS_NOSIZING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5ce48-142"><a href="common-control-versions.md">Version 6,00 und</a>höher.</span><span class="sxs-lookup"><span data-stu-id="5ce48-142"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="5ce48-143">Der Benutzer kann den unter Teiler nicht auf das Header Steuerelement ziehen.</span><span class="sxs-lookup"><span data-stu-id="5ce48-143">The user cannot drag the divider on the header control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <span data-ttu-id="5ce48-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5ce48-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5ce48-145"><a href="common-control-versions.md">Version 6,00 und</a>höher.</span><span class="sxs-lookup"><span data-stu-id="5ce48-145"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="5ce48-146">Eine Schaltfläche wird angezeigt, wenn nicht alle Elemente innerhalb des Rechtecks des Header Steuer Elements angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="5ce48-146">A button is displayed when not all items can be displayed within the header control's rectangle.</span></span> <span data-ttu-id="5ce48-147">Wenn Sie auf diese Schaltfläche klicken, wird eine <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> Benachrichtigung gesendet.</span><span class="sxs-lookup"><span data-stu-id="5ce48-147">When clicked, this button sends an <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> notification.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="5ce48-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ce48-148">Remarks</span></span>

<span data-ttu-id="5ce48-149">Wenn Sie die Stile nach dem Erstellen des Steuer Elements abrufen und ändern möchten, verwenden Sie die Funktionen [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) und [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="5ce48-149">To retrieve and change the styles after creating the control, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ce48-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ce48-150">Requirements</span></span>



| <span data-ttu-id="5ce48-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ce48-151">Requirement</span></span> | <span data-ttu-id="5ce48-152">Wert</span><span class="sxs-lookup"><span data-stu-id="5ce48-152">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce48-153">Header</span><span class="sxs-lookup"><span data-stu-id="5ce48-153">Header</span></span><br/> | <dl> <span data-ttu-id="5ce48-154"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ce48-154"><dt>CommCtrl.h</dt></span></span> </dl> |



