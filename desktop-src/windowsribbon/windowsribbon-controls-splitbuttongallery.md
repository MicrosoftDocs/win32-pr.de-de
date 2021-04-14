---
title: Split Button-Katalog
description: Die unterteilte Schaltflächen Galerie ist ein zusammengesetztes Steuerelement, das eine primär Schaltfläche enthält, die ein einzelnes Standardelement oder einen Standardbefehl verfügbar macht, und eine sekundäre Schaltfläche, auf die der Rest der Element-oder Befehls Auflistung in einer sich gegenseitig ausschließenden Dropdown Liste
ms.assetid: c0fcfe72-d2e9-465d-941a-b3832b36b8c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1865949c1b6f3e274b01d0b4e454dc42e619c2c0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104391113"
---
# <a name="split-button-gallery"></a><span data-ttu-id="616a1-103">Split Button-Katalog</span><span class="sxs-lookup"><span data-stu-id="616a1-103">Split Button Gallery</span></span>

<span data-ttu-id="616a1-104">Die unterteilte Schaltflächen Galerie ist ein zusammengesetztes Steuerelement, das eine primär Schaltfläche enthält, die ein einzelnes Standardelement oder einen Standardbefehl verfügbar macht, und eine sekundäre Schaltfläche, auf die der Rest der Element-oder Befehls Auflistung in einer sich gegenseitig ausschließenden Dropdown Liste</span><span class="sxs-lookup"><span data-stu-id="616a1-104">The Split Button Gallery is a composite control that contains a primary button which exposes a single default item or Command, and a secondary button which when clicked displays the rest of the item or Command collection in a mutually exclusive drop-down list.</span></span>

-   [<span data-ttu-id="616a1-105">Details</span><span class="sxs-lookup"><span data-stu-id="616a1-105">Details</span></span>](#details)
-   [<span data-ttu-id="616a1-106">Eigenschaften von "Split Button Gallery"</span><span class="sxs-lookup"><span data-stu-id="616a1-106">Split Button Gallery Properties</span></span>](#split-button-gallery-properties)
-   [<span data-ttu-id="616a1-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="616a1-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="616a1-108">Details</span><span class="sxs-lookup"><span data-stu-id="616a1-108">Details</span></span>

<span data-ttu-id="616a1-109">Dieses Steuerelement ist nützlich, um eng verwandte Elemente in Fällen verfügbar zu machen, in denen ein offensichtlicher Standard verfügbar ist und die einzelnen Elemente durch ein Bild, Text oder beides dargestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="616a1-109">This control is useful for exposing closely related items in cases where an obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="616a1-110">Der folgende Screenshot zeigt den Katalog mit der Menü Band Aufteilung in Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="616a1-110">The following screen shot illustrates the Ribbon Split Button Gallery in Microsoft Paint.</span></span>

![Screenshot eines splitbuttongallery-Steuer Elements im Microsoft Paint-Menüband.](images/controls/splitbuttongallery.png)

## <a name="split-button-gallery-properties"></a><span data-ttu-id="616a1-112">Eigenschaften von "Split Button Gallery"</span><span class="sxs-lookup"><span data-stu-id="616a1-112">Split Button Gallery Properties</span></span>

<span data-ttu-id="616a1-113">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Katalog Steuerelement für unterteilte Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="616a1-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Split Button Gallery control.</span></span>

<span data-ttu-id="616a1-114">In der Regel wird die Eigenschaft "Split Button Gallery" in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen-Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird</span><span class="sxs-lookup"><span data-stu-id="616a1-114">Typically, a Split Button Gallery property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="616a1-115">Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="616a1-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="616a1-116">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="616a1-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="616a1-117">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="616a1-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="616a1-118">In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="616a1-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="616a1-119">In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Steuerelement "Split Button Gallery" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="616a1-119">The following table lists the property keys that are associated with the Split Button Gallery control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="616a1-120">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="616a1-120">Property Key</span></span></th>
<th><span data-ttu-id="616a1-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="616a1-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="616a1-122"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span><span class="sxs-lookup"><span data-stu-id="616a1-122"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span></span></td>
<td><span data-ttu-id="616a1-123">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="616a1-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="616a1-124"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="616a1-124"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="616a1-125">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="616a1-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="616a1-126"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="616a1-126"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="616a1-127">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="616a1-127">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="616a1-128"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="616a1-128"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="616a1-129">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="616a1-129">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="616a1-130"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="616a1-130"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="616a1-131">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="616a1-131">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="616a1-132"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="616a1-132"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="616a1-133">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="616a1-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="616a1-134"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="616a1-134"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="616a1-135">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="616a1-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="616a1-136"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="616a1-136"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="616a1-137">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="616a1-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="616a1-138"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(nur gültig für einen Element Katalog)</span><span class="sxs-lookup"><span data-stu-id="616a1-138"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(only valid for an item gallery)</span></span><br/></td>
<td><span data-ttu-id="616a1-139">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="616a1-139">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="616a1-140">Wenn der Befehl, der dem Steuerelement zugeordnet ist, durch einen <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>iuiframework:: invalidateuicommand</strong></a>-Befehl ungültig gemacht wird, fragt das Framework diese Eigenschaft ab, wenn <code>UI_INVALIDATIONS_VALUE</code> als Wert von <em>Flags</em>übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="616a1-140">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="616a1-141"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="616a1-141"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="616a1-142">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="616a1-142">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="616a1-143"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="616a1-143"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="616a1-144">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="616a1-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="616a1-145"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="616a1-145"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="616a1-146">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="616a1-146">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="616a1-147"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="616a1-147"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="616a1-148">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="616a1-148">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="616a1-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="616a1-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="616a1-150">**Splitbuttongallery-Markup Element**</span><span class="sxs-lookup"><span data-stu-id="616a1-150">**SplitButtonGallery markup element**</span></span>](windowsribbon-element-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="616a1-151">Arbeiten mit Galerien</span><span class="sxs-lookup"><span data-stu-id="616a1-151">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="616a1-152">Galerie Beispiel</span><span class="sxs-lookup"><span data-stu-id="616a1-152">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

