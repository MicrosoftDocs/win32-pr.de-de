---
title: Erweiterte Toolbar-Stile (kommctrl. h)
description: In diesem Abschnitt werden die von Symbolleisten-Steuerelementen unterstützten erweiterten Stile aufgelistet
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056e48753485364017f04f7b84e609b19473bf5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354111"
---
# <a name="toolbar-extended-styles"></a><span data-ttu-id="26945-103">Erweiterte Toolbar-Stile</span><span class="sxs-lookup"><span data-stu-id="26945-103">Toolbar Extended Styles</span></span>

<span data-ttu-id="26945-104">In diesem Abschnitt werden die von Symbolleisten-Steuerelementen unterstützten erweiterten Stile aufgelistet</span><span class="sxs-lookup"><span data-stu-id="26945-104">This section lists the extended styles supported by toolbar controls.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="26945-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="26945-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="26945-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26945-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl> <span data-ttu-id="26945-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26945-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="26945-108"><a href="common-control-versions.md">Version 4,71</a>.</span><span class="sxs-lookup"><span data-stu-id="26945-108"><a href="common-control-versions.md">Version 4.71</a>.</span></span> <span data-ttu-id="26945-109">Dieser Stil ermöglicht, dass Schaltflächen über einen separaten Dropdown Pfeil verfügen.</span><span class="sxs-lookup"><span data-stu-id="26945-109">This style allows buttons to have a separate dropdown arrow.</span></span> <span data-ttu-id="26945-110">Schaltflächen, die den <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> Stil aufweisen, werden in einem separaten Abschnitt rechts von der Schaltfläche mit einem Dropdown Pfeil gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="26945-110">Buttons that have the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> style will be drawn with a dropdown arrow in a separate section, to the right of the button.</span></span> <span data-ttu-id="26945-111">Wenn auf den Pfeil geklickt wird, wird nur der Pfeil Teil der Schaltfläche dedrückt, und das Symbolleisten-Steuerelement sendet einen <a href="tbn-dropdown.md">TBN_DROPDOWN</a> Benachrichtigungs Code, um die Anwendung aufzufordern, das Dropdown Menü anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="26945-111">If the arrow is clicked, only the arrow portion of the button will depress, and the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code to prompt the application to display the dropdown menu.</span></span> <span data-ttu-id="26945-112">Wenn auf den Hauptteil der Schaltfläche geklickt wird, sendet das Symbolleisten-Steuerelement eine WM_COMMAND Meldung mit der ID der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="26945-112">If the main part of the button is clicked, the toolbar control sends a WM_COMMAND message with the button's ID.</span></span> <span data-ttu-id="26945-113">Die Anwendung antwortet normalerweise, indem der erste Befehl im Menü gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="26945-113">The application normally responds by launching the first command on the menu.</span></span><br/> <span data-ttu-id="26945-114">Es gibt viele Situationen, in denen Sie möglicherweise nur einige der Dropdown Schaltflächen auf einer Symbolleiste mit getrennten Pfeilen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="26945-114">There are many situations where you may want to have only some of the dropdown buttons on a toolbar with separated arrows.</span></span> <span data-ttu-id="26945-115">Legen Sie zu diesem Zweck den TBSTYLE_EX_DRAWDDARROWS erweiterten Stil fest.</span><span class="sxs-lookup"><span data-stu-id="26945-115">To do so, set the TBSTYLE_EX_DRAWDDARROWS extended style.</span></span> <span data-ttu-id="26945-116">Weisen Sie diese Schaltflächen, die keine getrennten Pfeile aufweisen, <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> Stil zu.</span><span class="sxs-lookup"><span data-stu-id="26945-116">Give those buttons that will not have separated arrows the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> style.</span></span> <span data-ttu-id="26945-117">Für Schaltflächen mit diesem Stil wird neben dem Bild ein Pfeil angezeigt.</span><span class="sxs-lookup"><span data-stu-id="26945-117">Buttons with this style will have an arrow displayed next to the image.</span></span> <span data-ttu-id="26945-118">Der Pfeil wird jedoch nicht getrennt. wenn auf einen beliebigen Teil der Schaltfläche geklickt wird, sendet das Symbolleisten-Steuerelement einen <a href="tbn-dropdown.md">TBN_DROPDOWN</a> Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="26945-118">However, the arrow will not be separate and when any part of the button is clicked, the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code.</span></span> <span data-ttu-id="26945-119">Um das Neuzeichnen von Problemen zu vermeiden, sollte dieser Stil festgelegt werden, bevor das ToolBar-Steuerelement sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="26945-119">To prevent repainting problems, this style should be set before the toolbar control becomes visible.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl> <span data-ttu-id="26945-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26945-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="26945-121"><a href="common-control-versions.md">Version 5,81</a>.</span><span class="sxs-lookup"><span data-stu-id="26945-121"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="26945-122">Dieser Stil verbirgt teilweise abgeschnittene Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="26945-122">This style hides partially clipped buttons.</span></span> <span data-ttu-id="26945-123">Dieser Stil wird am häufigsten für Symbolleisten verwendet, die Teil eines Grund leisten-Steuer Elements sind.</span><span class="sxs-lookup"><span data-stu-id="26945-123">The most common use of this style is for toolbars that are part of a rebar control.</span></span> <span data-ttu-id="26945-124">Wenn ein benachbartes Band einen Teil einer Schaltfläche abdeckt, wird die Schaltfläche nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="26945-124">If an adjacent band covers part of a button, the button will not be displayed.</span></span> <span data-ttu-id="26945-125">Wenn das Feld für die Bereichs Weitergabe jedoch den <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> Stil hat, wird die Schaltfläche im Dropdown Menü von Chevron angezeigt.</span><span class="sxs-lookup"><span data-stu-id="26945-125">However, if the rebar band has the <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> style, the button will be displayed on the chevron's dropdown menu.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl> <span data-ttu-id="26945-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26945-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="26945-127"><a href="common-control-versions.md">Version 6</a>.</span><span class="sxs-lookup"><span data-stu-id="26945-127"><a href="common-control-versions.md">Version 6</a>.</span></span> <span data-ttu-id="26945-128">Dieser Stil erfordert, dass die Symbolleiste doppelt gepuffert wird.</span><span class="sxs-lookup"><span data-stu-id="26945-128">This style requires the toolbar to be double buffered.</span></span> <span data-ttu-id="26945-129">Die doppelte Pufferung ist ein Mechanismus, der erkennt, wenn sich die Symbolleiste geändert hat.</span><span class="sxs-lookup"><span data-stu-id="26945-129">Double buffering is a mechanism that detects when the toolbar has changed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="26945-130">Comctl32.dll Version 6 ist nicht Verteil Bar, aber in Windows oder höher enthalten.</span><span class="sxs-lookup"><span data-stu-id="26945-130">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="26945-131">Wenn Sie Comctl32.dll Version 6 verwenden möchten, geben Sie ihn in einem Manifest an.</span><span class="sxs-lookup"><span data-stu-id="26945-131">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="26945-132">Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen</a>.</span><span class="sxs-lookup"><span data-stu-id="26945-132">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl> <span data-ttu-id="26945-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26945-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="26945-134"><a href="common-control-versions.md">Version 5,81</a>.</span><span class="sxs-lookup"><span data-stu-id="26945-134"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="26945-135">Mit diesem Stil können Sie Text für alle Schaltflächen festlegen, ihn aber nur für diese Schaltflächen mit dem <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> Schaltflächen Stil anzeigen.</span><span class="sxs-lookup"><span data-stu-id="26945-135">This style allows you to set text for all buttons, but only display it for those buttons with the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> button style.</span></span> <span data-ttu-id="26945-136">Der <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> Stil muss ebenfalls festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="26945-136">The <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> style must also be set.</span></span> <span data-ttu-id="26945-137">Wenn eine Schaltfläche keinen Text anzeigt, muss die Anwendung normalerweise <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> oder <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> verarbeiten, um eine QuickInfo anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="26945-137">Normally, when a button does not display text, your application must handle <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> or <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> to display a tooltip.</span></span> <span data-ttu-id="26945-138">Beim erweiterten TBSTYLE_EX_MIXEDBUTTONS Stil wird Text, der festgelegt, aber nicht auf einer Schaltfläche angezeigt wird, automatisch als QuickInfo-Text der Schaltfläche verwendet.</span><span class="sxs-lookup"><span data-stu-id="26945-138">With the TBSTYLE_EX_MIXEDBUTTONS extended style, text that is set but not displayed on a button will automatically be used as the button's tooltip text.</span></span> <span data-ttu-id="26945-139">Die Anwendung muss nur TBN_GETINFOTIP oder oder TTN_GETDISPINFO verarbeiten, wenn Sie mehr Flexibilität bei der Angabe des QuickInfo-Texts benötigt.</span><span class="sxs-lookup"><span data-stu-id="26945-139">Your application only needs to handle TBN_GETINFOTIP or or TTN_GETDISPINFO if it needs more flexibility in specifying the tooltip text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl> <span data-ttu-id="26945-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26945-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="26945-141"><a href="common-control-versions.md">Version 5,82</a>.</span><span class="sxs-lookup"><span data-stu-id="26945-141"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="26945-142"><strong>Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.</strong></span><span class="sxs-lookup"><span data-stu-id="26945-142"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="26945-143">Dieser Stil gibt der Symbolleiste eine vertikale Ausrichtung und organisiert die Symbolleisten Schaltflächen in Spalten.</span><span class="sxs-lookup"><span data-stu-id="26945-143">This style gives the toolbar a vertical orientation and organizes the toolbar buttons into columns.</span></span> <span data-ttu-id="26945-144">Die Schaltflächen werden vertikal vertikal dargestellt, bis eine Schaltfläche die umgebende Höhe der Symbolleiste überschreitet (siehe <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), und anschließend wird eine neue Spalte erstellt.</span><span class="sxs-lookup"><span data-stu-id="26945-144">The buttons flow down vertically until a button has exceeded the bounding height of the toolbar (see <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), and then a new column is created.</span></span> <span data-ttu-id="26945-145">Die Symbolleiste fließt auf diese Weise, bis alle Schaltflächen positioniert sind.</span><span class="sxs-lookup"><span data-stu-id="26945-145">The toolbar flows the buttons in this manner until all buttons are positioned.</span></span> <span data-ttu-id="26945-146">Um dieses Format zu verwenden, muss der TBSTYLE_EX_VERTICAL Stil ebenfalls festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="26945-146">To use this style, the TBSTYLE_EX_VERTICAL style must also be set.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="26945-147">Dieser Stil wird in zukünftigen Versionen von Comctl32.dll möglicherweise nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="26945-147">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="26945-148">Außerdem ist dieser Stil nicht in "kommctrl. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="26945-148">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="26945-149">Fügen Sie die folgende Definition zu den Quelldateien Ihrer Anwendung hinzu, um diesen Stil zu verwenden: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span><span class="sxs-lookup"><span data-stu-id="26945-149">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span></span></blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl> <span data-ttu-id="26945-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26945-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="26945-151"><a href="common-control-versions.md">Version 5,82</a>.</span><span class="sxs-lookup"><span data-stu-id="26945-151"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="26945-152"><strong>Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.</strong></span><span class="sxs-lookup"><span data-stu-id="26945-152"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="26945-153">Dieser Stil gibt der Symbolleiste eine vertikale Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="26945-153">This style gives the toolbar a vertical orientation.</span></span> <span data-ttu-id="26945-154">Die Symbolleisten Schaltflächen werden von oben nach unten statt horizontal weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="26945-154">Toolbar buttons flow from top to bottom instead of horizontally.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="26945-155">Dieser Stil wird in zukünftigen Versionen von Comctl32.dll möglicherweise nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="26945-155">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="26945-156">Außerdem ist dieser Stil nicht in "kommctrl. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="26945-156">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="26945-157">Fügen Sie die folgende Definition zu den Quelldateien Ihrer Anwendung hinzu, um diesen Stil zu verwenden: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span><span class="sxs-lookup"><span data-stu-id="26945-157">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span></span></blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="26945-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26945-158">Remarks</span></span>

<span data-ttu-id="26945-159">Um einen erweiterten Stil festzulegen, senden Sie das Symbolleisten-Steuerelement an eine [**TB- \_ SetExtendedStyle**](tb-setextendedstyle.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="26945-159">To set an extended style, send the toolbar control a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span> <span data-ttu-id="26945-160">Wenn Sie bestimmen möchten, welche erweiterten Stile aktuell festgelegt sind, senden Sie eine [**TB- \_ GetExtendedStyle**](tb-getextendedstyle.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="26945-160">To determine what extended styles are currently set, send a [**TB\_GETEXTENDEDSTYLE**](tb-getextendedstyle.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="26945-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26945-161">Requirements</span></span>



| <span data-ttu-id="26945-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26945-162">Requirement</span></span> | <span data-ttu-id="26945-163">Wert</span><span class="sxs-lookup"><span data-stu-id="26945-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26945-164">Header</span><span class="sxs-lookup"><span data-stu-id="26945-164">Header</span></span><br/> | <dl> <span data-ttu-id="26945-165"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="26945-165"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





