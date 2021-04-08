---
title: Schaltfläche (Windows-Menü Band Framework)
description: Die Schaltfläche ist ein Steuerelement, auf das der Benutzer klicken kann, um Eingaben für eine Anwendung bereitzustellen.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102646"
---
# <a name="button-windows-ribbon-framework"></a><span data-ttu-id="3c1f8-103">Schaltfläche (Windows-Menü Band Framework)</span><span class="sxs-lookup"><span data-stu-id="3c1f8-103">Button (Windows Ribbon Framework)</span></span>

<span data-ttu-id="3c1f8-104">Die Schaltfläche ist ein Steuerelement, auf das der Benutzer klicken kann, um Eingaben für eine Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-104">The Button is a control the user can click to provide input to an application.</span></span>

-   [<span data-ttu-id="3c1f8-105">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="3c1f8-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="3c1f8-106">Schaltflächen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c1f8-106">Button Properties</span></span>](#button-properties)
-   [<span data-ttu-id="3c1f8-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c1f8-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="3c1f8-108">Einführung</span><span class="sxs-lookup"><span data-stu-id="3c1f8-108">Introduction</span></span>

<span data-ttu-id="3c1f8-109">Der folgende Screenshot enthält drei Beispiele für das Menüband-Schaltflächen Element.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-109">The following screen shot contains three examples of the Ribbon Button element.</span></span>

![Screenshot der Schaltflächen-Steuerelemente im Microsoft WordPad-Menüband.](images/controls/button.png)

## <a name="button-properties"></a><span data-ttu-id="3c1f8-111">Schaltflächen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c1f8-111">Button Properties</span></span>

<span data-ttu-id="3c1f8-112">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Schaltflächen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Button control.</span></span>

<span data-ttu-id="3c1f8-113">In der Regel wird eine Schaltflächen Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-113">Typically, a Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="3c1f8-114">Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="3c1f8-115">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="3c1f8-116">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="3c1f8-117">In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="3c1f8-118">In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Schaltflächen-Steuerelement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-118">The following table lists the property keys that are associated with the Button control.</span></span>



| <span data-ttu-id="3c1f8-119">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="3c1f8-119">Property Key</span></span>                                                                                             | <span data-ttu-id="3c1f8-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c1f8-120">Notes</span></span>                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c1f8-121">UI- \_ pkey \_ aktiviert</span><span class="sxs-lookup"><span data-stu-id="3c1f8-121">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                               | <span data-ttu-id="3c1f8-122">Unterstützt [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) und [**iuiframework:: abtuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="3c1f8-122">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="3c1f8-123">UI- \_ pkey- \_ KeyTip</span><span class="sxs-lookup"><span data-stu-id="3c1f8-123">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                 | <span data-ttu-id="3c1f8-124">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-124">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="3c1f8-125">UI- \_ pkey- \_ Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="3c1f8-125">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                                   | <span data-ttu-id="3c1f8-126">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-126">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="3c1f8-127">UI \_ pkey \_ labeldescription</span><span class="sxs-lookup"><span data-stu-id="3c1f8-127">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)             | <span data-ttu-id="3c1f8-128">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-128">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="3c1f8-129">UI \_ pkey \_ largehighkontra stimage</span><span class="sxs-lookup"><span data-stu-id="3c1f8-129">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | <span data-ttu-id="3c1f8-130">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="3c1f8-131">UI \_ pkey \_ largeimage</span><span class="sxs-lookup"><span data-stu-id="3c1f8-131">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)                         | <span data-ttu-id="3c1f8-132">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="3c1f8-133">UI \_ pkey \_ smallhighkontra stimage</span><span class="sxs-lookup"><span data-stu-id="3c1f8-133">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | <span data-ttu-id="3c1f8-134">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="3c1f8-135">UI \_ pkey \_ smallImage</span><span class="sxs-lookup"><span data-stu-id="3c1f8-135">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)                         | <span data-ttu-id="3c1f8-136">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="3c1f8-137">UI- \_ pkey- \_ tooltipdescription</span><span class="sxs-lookup"><span data-stu-id="3c1f8-137">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | <span data-ttu-id="3c1f8-138">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-138">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="3c1f8-139">UI- \_ pkey- \_ ToolTipTitle</span><span class="sxs-lookup"><span data-stu-id="3c1f8-139">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | <span data-ttu-id="3c1f8-140">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c1f8-140">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="3c1f8-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c1f8-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c1f8-142">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3c1f8-142">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="3c1f8-143">**Button-Markup Element**</span><span class="sxs-lookup"><span data-stu-id="3c1f8-143">**Button markup element**</span></span>](windowsribbon-element-button.md)
</dt> </dl>

 

 
