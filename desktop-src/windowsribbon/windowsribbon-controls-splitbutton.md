---
title: Unterteilte Schaltfläche
description: Die unterteilte Schaltfläche ist ein zusammengesetztes Steuerelement, mit dem der Benutzer einen Standardwert auswählen kann, der an eine primär Schaltfläche gebunden ist, oder aus einer Liste von sich gegenseitig ausschließenden Werten auswählen, die in einer Dropdown Liste an eine sekundäre Schaltfläche
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b78aa261eebb24404eeaf8b3fdad7f630331f58
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106341565"
---
# <a name="split-button"></a><span data-ttu-id="7c828-103">Unterteilte Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="7c828-103">Split Button</span></span>

<span data-ttu-id="7c828-104">Die unterteilte Schaltfläche ist ein zusammengesetztes Steuerelement, mit dem der Benutzer einen Standardwert auswählen kann, der an eine primär Schaltfläche gebunden ist, oder aus einer Liste von sich gegenseitig ausschließenden Werten auswählen, die in einer Dropdown Liste an eine sekundäre Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="7c828-104">The Split Button is a composite control with which the user can select a default value bound to a primary button, or select from a list of mutually exclusive values displayed in a drop-down list bound to a secondary button.</span></span>

-   [<span data-ttu-id="7c828-105">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="7c828-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="7c828-106">Eigenschaften für getrennte Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="7c828-106">Split Button Properties</span></span>](#split-button-properties)
-   [<span data-ttu-id="7c828-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7c828-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="7c828-108">Einführung</span><span class="sxs-lookup"><span data-stu-id="7c828-108">Introduction</span></span>

<span data-ttu-id="7c828-109">Dieses Steuerelement ist nützlich, um eng verwandte Elemente in Fällen verfügbar zu machen, in denen ein offensichtlicher Standard verfügbar ist und die einzelnen Elemente durch ein Bild, Text oder beides dargestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="7c828-109">This control is useful for exposing closely related items in cases where an obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="7c828-110">Der folgende Screenshot veranschaulicht die unterteilte Schaltfläche des Menübands.</span><span class="sxs-lookup"><span data-stu-id="7c828-110">The following screen shot illustrates the Ribbon Split Button.</span></span>

![Screenshot eines SplitButton-Steuer Elements in einem beispielmenüband.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a><span data-ttu-id="7c828-112">Eigenschaften für getrennte Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="7c828-112">Split Button Properties</span></span>

<span data-ttu-id="7c828-113">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Steuerelement unterteilte Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="7c828-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Split Button control.</span></span>

<span data-ttu-id="7c828-114">In der Regel wird eine unterteilte Schaltflächen Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="7c828-114">Typically, a Split Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="7c828-115">Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="7c828-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="7c828-116">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="7c828-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="7c828-117">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7c828-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="7c828-118">In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7c828-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="7c828-119">In der folgenden Tabelle werden die Eigenschaften Schlüssel aufgelistet, die dem Steuerelement für die unterteilte Schaltfläche zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7c828-119">The following table lists the property keys that are associated with the Split Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7c828-120">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="7c828-120">Property Key</span></span></th>
<th><span data-ttu-id="7c828-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c828-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7c828-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="7c828-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="7c828-123">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7c828-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span><br/> <span data-ttu-id="7c828-124">Wenn alle untergeordneten Elemente deaktiviert sind, legt das Framework <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> auf false (0) fest.</span><span class="sxs-lookup"><span data-stu-id="7c828-124">If all child items are disabled, the framework sets <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> to false (0).</span></span> <span data-ttu-id="7c828-125">Wenn ein oder mehrere untergeordnete Elemente aktiviert sind, wird UI_PKEY_Enabled auf true (-1) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7c828-125">Otherwise, if one or more child items are enabled, UI_PKEY_Enabled is set to true (-1).</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="7c828-126">Die <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> -Eigenschaft für das Steuerelement für die unterteilte Schaltfläche sollte ungültig werden, nachdem mindestens ein untergeordnetes Element aktiviert oder deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="7c828-126">The <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> property for the Split Button control should be invalidated after one or more child items are enabled or disabled.</span></span> <span data-ttu-id="7c828-127">Dadurch wird sichergestellt, dass das Framework den aktualisierten Eigenschafts Wert abfragt und den Zustand des Steuer Elements unterteilte Schaltflächen auf der Multifunktionsleisten-Benutzeroberfläche aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7c828-127">This ensures that the framework queries the updated property value and refreshes the state of the Split Button control in the ribbon UI.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c828-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="7c828-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="7c828-129">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7c828-129">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7c828-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="7c828-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="7c828-131">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7c828-131">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c828-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="7c828-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="7c828-133">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7c828-133">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7c828-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7c828-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c828-135">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7c828-135">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="7c828-136">**SplitButton-Markup Element**</span><span class="sxs-lookup"><span data-stu-id="7c828-136">**SplitButton markup element**</span></span>](windowsribbon-element-splitbutton.md)
</dt> </dl>