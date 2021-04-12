---
title: Registerkarten Gruppe
description: Eine Registerkarten Gruppe ist ein kontextbezogenes Steuerelement, das zur Laufzeit auf Grundlage eines Dokument-oder Arbeitsbereichs Zustands ausgeblendet oder angezeigt wird. Die Registerkarten Gruppe enthält einen Satz kontextbezogener Registerkarten-Steuerelemente.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316010"
---
# <a name="tab-group"></a><span data-ttu-id="d7167-104">Registerkarten Gruppe</span><span class="sxs-lookup"><span data-stu-id="d7167-104">Tab Group</span></span>

<span data-ttu-id="d7167-105">Eine Registerkarten Gruppe ist ein kontextbezogenes Steuerelement, das zur Laufzeit auf Grundlage eines Dokument-oder Arbeitsbereichs Zustands ausgeblendet oder angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7167-105">A Tab Group is a contextual control that is hidden or displayed at run time, based on a document or workspace state.</span></span> <span data-ttu-id="d7167-106">Die Registerkarten Gruppe enthält einen Satz kontextbezogener [Register](windowsribbon-controls-tab.md) Karten-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="d7167-106">The Tab Group contains a set of context-related [Tab](windowsribbon-controls-tab.md) controls.</span></span>

-   [<span data-ttu-id="d7167-107">Details</span><span class="sxs-lookup"><span data-stu-id="d7167-107">Details</span></span>](#details)
-   [<span data-ttu-id="d7167-108">Registerkarten Gruppen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7167-108">Tab Group Properties</span></span>](#tab-group-properties)
-   [<span data-ttu-id="d7167-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7167-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="d7167-110">Details</span><span class="sxs-lookup"><span data-stu-id="d7167-110">Details</span></span>

<span data-ttu-id="d7167-111">In der Regel wird eine Registerkarten Gruppe in bestimmten Dokument-oder Arbeitsbereichs Zuständen angezeigt, z. b. Wenn ein Benutzer einen bestimmten Objekttyp auswählt.</span><span class="sxs-lookup"><span data-stu-id="d7167-111">Typically, a Tab Group is displayed during specific document or workspace states, such as when a user selects a particular object type.</span></span> <span data-ttu-id="d7167-112">Die Auswahl eines Bilds, das im Header einer Tabelle enthalten ist, kann z. b. erfordern, dass verschiedene Kontext Registerkarten angezeigt werden, die sowohl die Tabellen-als auch die Bild Funktionalität verfügbar machen</span><span class="sxs-lookup"><span data-stu-id="d7167-112">For example, the selection of an image contained in the header of a table might require various contextual tabs to be displayed that expose both table and image functionality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7167-113">Eine Registerkarten Gruppe unterstützt keine [Anwendungsmodi](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="d7167-113">A Tab Group does not support [application modes](ribbon-applicationmodes.md).</span></span> <span data-ttu-id="d7167-114">Allerdings können die einzelnen [Register](windowsribbon-controls-tab.md) Karten-Steuerelemente in einer Registerkarten Gruppe angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d7167-114">However, the individual [Tab](windowsribbon-controls-tab.md) controls within a Tab Group may.</span></span>

 

<span data-ttu-id="d7167-115">Der folgende Screenshot zeigt eine Kontext [Registerkarte](windowsribbon-controls-tab.md) aus Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="d7167-115">The following screen shot shows a contextual [Tab](windowsribbon-controls-tab.md) from Windows 7 Paint.</span></span>

![Screenshot, der ein Kontext abhängiges Registerkarten-Steuerelement anzeigt.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a><span data-ttu-id="d7167-117">Registerkarten Gruppen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7167-117">Tab Group Properties</span></span>

<span data-ttu-id="d7167-118">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Registerkarten Gruppen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d7167-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab Group control.</span></span>

<span data-ttu-id="d7167-119">In der Regel wird eine Registerkarten-Gruppen Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="d7167-119">Typically, a Tab Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="d7167-120">Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="d7167-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="d7167-121">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7167-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="d7167-122">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7167-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="d7167-123">In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d7167-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="d7167-124">In der folgenden Tabelle werden die Eigenschaften Schlüssel aufgelistet, die dem Registerkarten-Gruppen Steuerelement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d7167-124">The following table lists the property keys that are associated with the Tab Group control.</span></span>



| <span data-ttu-id="d7167-125">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d7167-125">Property Key</span></span>                                                                                     | <span data-ttu-id="d7167-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7167-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7167-127">UI \_ pkey \_ contextavailable</span><span class="sxs-lookup"><span data-stu-id="d7167-127">UI\_PKEY\_ContextAvailable</span></span>](windowsribbon-reference-properties-uipkey-contextavailable.md)     | <span data-ttu-id="d7167-128">Unterstützt [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) und [**iuiframework:: abtuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="d7167-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="d7167-129">UI- \_ pkey- \_ KeyTip</span><span class="sxs-lookup"><span data-stu-id="d7167-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="d7167-130">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7167-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="d7167-131">UI- \_ pkey- \_ Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="d7167-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="d7167-132">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7167-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="d7167-133">UI- \_ pkey- \_ tooltipdescription</span><span class="sxs-lookup"><span data-stu-id="d7167-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="d7167-134">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7167-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="d7167-135">UI- \_ pkey- \_ ToolTipTitle</span><span class="sxs-lookup"><span data-stu-id="d7167-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="d7167-136">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7167-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="d7167-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7167-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7167-138">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d7167-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="d7167-139">**TabGroup-Markup Element**</span><span class="sxs-lookup"><span data-stu-id="d7167-139">**TabGroup markup element**</span></span>](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 