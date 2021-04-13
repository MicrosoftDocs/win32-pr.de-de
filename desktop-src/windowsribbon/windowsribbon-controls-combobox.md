---
title: Kombinations Feld (Windows-Menü Band Framework)
description: Das Kombinations Feld besteht aus einem einspaltigen Listenfeld, das eine Auflistung von sich gegenseitig ausschließenden Elementen oder Befehlen enthält, kombiniert mit einem statischen Steuerelement oder einem Bearbeitungs Steuerelement und einem Dropdown Pfeil.
ms.assetid: 6b7de2ec-dcb7-44cb-b01f-db1ba0643499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c61c19963811d12557beafe3c5cff314c927ae7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474850"
---
# <a name="combo-box-windows-ribbon-framework"></a><span data-ttu-id="a9440-103">Kombinations Feld (Windows-Menü Band Framework)</span><span class="sxs-lookup"><span data-stu-id="a9440-103">Combo Box (Windows Ribbon Framework)</span></span>

<span data-ttu-id="a9440-104">Das Kombinations Feld besteht aus einem einspaltigen Listenfeld, das eine Auflistung von sich gegenseitig ausschließenden Elementen oder Befehlen enthält, kombiniert mit einem statischen Steuerelement oder einem Bearbeitungs Steuerelement und einem Dropdown Pfeil.</span><span class="sxs-lookup"><span data-stu-id="a9440-104">The Combo Box consists of a single-column list box that contains a collection of mutually exclusive items or Commands combined with a static or edit control and a drop-down arrow.</span></span> <span data-ttu-id="a9440-105">Der Listenfeld Bereich des Steuer Elements wird angezeigt, wenn der Benutzer auf den Dropdown Pfeil klickt.</span><span class="sxs-lookup"><span data-stu-id="a9440-105">The list box portion of the control is displayed when the user clicks the drop-down arrow.</span></span>

-   [<span data-ttu-id="a9440-106">Details</span><span class="sxs-lookup"><span data-stu-id="a9440-106">Details</span></span>](#details)
-   [<span data-ttu-id="a9440-107">Kombinations Feldeigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9440-107">Combo Box Properties</span></span>](#combo-box-properties)
-   [<span data-ttu-id="a9440-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9440-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="a9440-109">Details</span><span class="sxs-lookup"><span data-stu-id="a9440-109">Details</span></span>

<span data-ttu-id="a9440-110">Das aktuell ausgewählte Element oder der Befehl (sofern vorhanden) im Listenfeld wird im Steuerelement "statisch" oder "Bearbeiten" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a9440-110">The currently selected item or Command (if any) in the list box is displayed in the static or edit control.</span></span> <span data-ttu-id="a9440-111">Wenn der Benutzer die anfänglichen Zeichen eines vorhandenen Elements oder Befehls mit einem Bearbeitungs Steuerelement eingibt, wird das erste Element mit den ersten Zeichen im Listenfeld hervorgehoben, und der Eintrag im Bearbeitungs Steuerelement wird automatisch vervollständigt.</span><span class="sxs-lookup"><span data-stu-id="a9440-111">With an edit control, if the user types the initial characters of an existing item or Command, the list box will highlight the first item with those initial characters and autocomplete the entry in the edit control.</span></span>

<span data-ttu-id="a9440-112">Unterstützt nur eine vertikale Zieh Punkt Leiste oder ein Handle für die Größe der Größe.</span><span class="sxs-lookup"><span data-stu-id="a9440-112">Supports a vertical gripper bar, or resizing handle, only.</span></span>

<span data-ttu-id="a9440-113">Dieses Steuerelement ist nützlich, um einfache, eng verwandte Textelemente verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="a9440-113">This control is useful for exposing simple, closely related text items.</span></span>

<span data-ttu-id="a9440-114">Der folgende Screenshot veranschaulicht das Menüband-Kombinations Feld in Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="a9440-114">The following screen shot illustrates the Ribbon Combo Box in Live Movie Maker.</span></span>

![Screenshot eines ComboBox-Steuer Elements im Microsoft Paint-Menüband.](images/controls/combobox.png)

## <a name="combo-box-properties"></a><span data-ttu-id="a9440-116">Kombinations Feldeigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9440-116">Combo Box Properties</span></span>

<span data-ttu-id="a9440-117">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Kombinations Feld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a9440-117">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Combo Box control.</span></span>

<span data-ttu-id="a9440-118">In der Regel wird eine Kombinations Feld Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="a9440-118">Typically, a Combo Box property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="a9440-119">Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="a9440-119">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="a9440-120">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="a9440-120">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="a9440-121">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a9440-121">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="a9440-122">In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a9440-122">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="a9440-123">In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Kombinations Feld-Steuerelement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a9440-123">The following table lists the property keys that are associated with the Combo Box control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9440-124">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="a9440-124">Property Key</span></span></th>
<th><span data-ttu-id="a9440-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9440-125">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9440-126"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="a9440-126"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="a9440-127">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a9440-127">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9440-128"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="a9440-128"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="a9440-129">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a9440-129">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9440-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="a9440-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="a9440-131">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a9440-131">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9440-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="a9440-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="a9440-133">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9440-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9440-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="a9440-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="a9440-135">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9440-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9440-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="a9440-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="a9440-137">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9440-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9440-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="a9440-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="a9440-139">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9440-139">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9440-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span><span class="sxs-lookup"><span data-stu-id="a9440-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span></span></td>
<td><span data-ttu-id="a9440-141">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a9440-141">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9440-142"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="a9440-142"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="a9440-143">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9440-143">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9440-144"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="a9440-144"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="a9440-145">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9440-145">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9440-146"><a href="windowsribbon-reference-properties-uipkey-stringvalue.md">UI_PKEY_StringValue</a></span><span class="sxs-lookup"><span data-stu-id="a9440-146"><a href="windowsribbon-reference-properties-uipkey-stringvalue.md">UI_PKEY_StringValue</a></span></span></td>
<td><span data-ttu-id="a9440-147">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a9440-147">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="a9440-148">Wenn der Befehl, der dem Steuerelement zugeordnet ist, durch einen <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>iuiframework:: invalidateuicommand</strong></a>-Befehl ungültig gemacht wird, fragt das Framework diese Eigenschaft ab, wenn <code>UI_INVALIDATIONS_VALUE</code> als Wert von <em>Flags</em>übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a9440-148">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9440-149"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="a9440-149"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="a9440-150">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9440-150">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9440-151"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="a9440-151"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="a9440-152">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9440-152">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a9440-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9440-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9440-154">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a9440-154">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="a9440-155">**ComboBox-Markup Element**</span><span class="sxs-lookup"><span data-stu-id="a9440-155">**ComboBox markup element**</span></span>](windowsribbon-element-combobox.md)
</dt> <dt>

[<span data-ttu-id="a9440-156">Arbeiten mit Galerien</span><span class="sxs-lookup"><span data-stu-id="a9440-156">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="a9440-157">Galerie Beispiel</span><span class="sxs-lookup"><span data-stu-id="a9440-157">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

