---
title: Kontrollkästchen
description: Das Kontrollkästchen ist ein Steuerelement, auf das der Benutzer klicken kann, um Eingaben für eine Anwendung bereitzustellen. Das-Steuerelement stellt einen visuellen UMSCHALT Zustand dar, der visuell dargestellt wird.
ms.assetid: fe07aa5c-1818-41e2-b48d-5fefe50d733f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e283facf81e8c3d2adad670329fcf0cf168d09
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732760"
---
# <a name="check-box"></a><span data-ttu-id="31cbd-104">Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="31cbd-104">Check Box</span></span>

<span data-ttu-id="31cbd-105">Das Kontrollkästchen ist ein Steuerelement, auf das der Benutzer klicken kann, um Eingaben für eine Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="31cbd-105">The Check Box is a control the user can click to provide input to an application.</span></span> <span data-ttu-id="31cbd-106">Das-Steuerelement stellt einen visuellen UMSCHALT Zustand dar, der visuell dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="31cbd-106">The control provides a toggle state that is represented visually.</span></span>

-   [<span data-ttu-id="31cbd-107">Details</span><span class="sxs-lookup"><span data-stu-id="31cbd-107">Details</span></span>](#details)
-   [<span data-ttu-id="31cbd-108">Kontrollkästchen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31cbd-108">Check Box Properties</span></span>](#check-box-properties)
-   [<span data-ttu-id="31cbd-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="31cbd-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="31cbd-110">Details</span><span class="sxs-lookup"><span data-stu-id="31cbd-110">Details</span></span>

<span data-ttu-id="31cbd-111">Das Kontrollkästchen unterstützt keinen tertiären bzw. unbestimmten Zustand.</span><span class="sxs-lookup"><span data-stu-id="31cbd-111">The Check Box does not support a tertiary, or indeterminate, state.</span></span>

<span data-ttu-id="31cbd-112">Der folgende Screenshot veranschaulicht das Kontrollkästchen-Element des Menübands.</span><span class="sxs-lookup"><span data-stu-id="31cbd-112">The following screen shot illustrates the Ribbon Check Box element.</span></span>

![Screenshot eines CheckBox-Steuer Elements im Microsoft Paint-Menüband.](images/controls/checkbox.png)

## <a name="check-box-properties"></a><span data-ttu-id="31cbd-114">Kontrollkästchen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31cbd-114">Check Box Properties</span></span>

<span data-ttu-id="31cbd-115">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Kontrollkästchen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="31cbd-115">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Check Box control.</span></span>

<span data-ttu-id="31cbd-116">In der Regel wird eine Kontrollkästchen Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="31cbd-116">Typically, a Check Box property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="31cbd-117">Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="31cbd-117">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="31cbd-118">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="31cbd-118">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="31cbd-119">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="31cbd-119">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="31cbd-120">In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="31cbd-120">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="31cbd-121">In der folgenden Tabelle werden die Eigenschaften Schlüssel aufgelistet, die dem Kontrollkästchen-Steuerelement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="31cbd-121">The following table lists the property keys that are associated with the Check Box control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="31cbd-122">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="31cbd-122">Property Key</span></span></th>
<th><span data-ttu-id="31cbd-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="31cbd-123">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31cbd-124"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span><span class="sxs-lookup"><span data-stu-id="31cbd-124"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span></span></td>
<td><span data-ttu-id="31cbd-125">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="31cbd-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="31cbd-126">Wenn der Befehl, der dem Steuerelement zugeordnet ist, durch einen <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>iuiframework:: invalidateuicommand</strong></a>-Befehl ungültig gemacht wird, fragt das Framework diese Eigenschaft ab, wenn <code>UI_INVALIDATIONS_VALUE</code> als Wert von <em>Flags</em>übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="31cbd-126">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31cbd-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="31cbd-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="31cbd-128">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="31cbd-128">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31cbd-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="31cbd-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="31cbd-130">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="31cbd-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31cbd-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="31cbd-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="31cbd-132">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="31cbd-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31cbd-133"><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></span><span class="sxs-lookup"><span data-stu-id="31cbd-133"><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></span></span></td>
<td><span data-ttu-id="31cbd-134">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="31cbd-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31cbd-135"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="31cbd-135"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="31cbd-136">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="31cbd-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31cbd-137"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="31cbd-137"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="31cbd-138">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="31cbd-138">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31cbd-139"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="31cbd-139"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="31cbd-140">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="31cbd-140">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31cbd-141"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="31cbd-141"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="31cbd-142">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="31cbd-142">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31cbd-143"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="31cbd-143"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="31cbd-144">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="31cbd-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31cbd-145"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="31cbd-145"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="31cbd-146">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="31cbd-146">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="31cbd-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="31cbd-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31cbd-148">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="31cbd-148">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="31cbd-149">**CheckBox-Markup Element**</span><span class="sxs-lookup"><span data-stu-id="31cbd-149">**CheckBox markup element**</span></span>](windowsribbon-element-checkbox.md)
</dt> </dl>

