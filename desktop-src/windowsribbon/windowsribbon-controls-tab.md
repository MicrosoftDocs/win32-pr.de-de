---
title: Registerkarte (Windows-Menü Band Framework)
description: Eine Registerkarte enthält Gruppen von verknüpften Steuerelementen.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340248"
---
# <a name="tab-windows-ribbon-framework"></a><span data-ttu-id="451bd-103">Registerkarte (Windows-Menü Band Framework)</span><span class="sxs-lookup"><span data-stu-id="451bd-103">Tab (Windows Ribbon Framework)</span></span>

<span data-ttu-id="451bd-104">Eine Registerkarte enthält [Gruppen](windowsribbon-controls-group.md) von verknüpften Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="451bd-104">A Tab contains [groups](windowsribbon-controls-group.md) of related controls.</span></span>

-   [<span data-ttu-id="451bd-105">Details</span><span class="sxs-lookup"><span data-stu-id="451bd-105">Details</span></span>](#details)
-   [<span data-ttu-id="451bd-106">Registerkarteneigenschaften</span><span class="sxs-lookup"><span data-stu-id="451bd-106">Tab Properties</span></span>](#tab-properties)
-   [<span data-ttu-id="451bd-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="451bd-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="451bd-108">Details</span><span class="sxs-lookup"><span data-stu-id="451bd-108">Details</span></span>

<span data-ttu-id="451bd-109">Es gibt drei Arten von Registerkarten im Menüband-Framework.</span><span class="sxs-lookup"><span data-stu-id="451bd-109">There are three types of Tab in the Ribbon framework.</span></span>



| <span data-ttu-id="451bd-110">type</span><span class="sxs-lookup"><span data-stu-id="451bd-110">Type</span></span>               | <span data-ttu-id="451bd-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="451bd-111">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="451bd-112">**Kern Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="451bd-112">**Core tab**</span></span>       | <span data-ttu-id="451bd-113">Kern Registerkarten, die die Standardfunktionen der Anwendung organisieren.</span><span class="sxs-lookup"><span data-stu-id="451bd-113">Core tabs that organize the default functions of the application.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="451bd-114">**Kontext Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="451bd-114">**Contextual tab**</span></span> | <span data-ttu-id="451bd-115">Registerkarten, die in bestimmten Dokument-oder Arbeitsbereichs Zuständen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="451bd-115">Tabs that are displayed during specific document or workspace states.</span></span> <span data-ttu-id="451bd-116">Wenn ein Benutzer beispielsweise einen bestimmten Objekttyp auswählt, z. b. ein Bild, das im Header einer Tabelle enthalten ist, werden möglicherweise verschiedene Kontext Registerkarten angezeigt, die sowohl die Tabellen-als auch die Bild Funktionalität verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="451bd-116">For example, if a user selects a particular object type, such as an image contained in the header of a table, then various contextual tabs might be displayed that expose both table and image functionality.</span></span> |
| <span data-ttu-id="451bd-117">**Modale Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="451bd-117">**Modal tab**</span></span>      | <span data-ttu-id="451bd-118">Kern Registerkarten, die in einem bestimmten Dokument-oder Arbeitsbereichs [Anwendungsmodus](ribbon-applicationmodes.md)angezeigt werden, z. b. in der Druckvorschau.</span><span class="sxs-lookup"><span data-stu-id="451bd-118">Core tabs that are displayed during a specific document or workspace [application mode](ribbon-applicationmodes.md), such as print preview.</span></span>                                                                                                                                        |



 

<span data-ttu-id="451bd-119">Der folgende Screenshot zeigt eine Kern Registerkarte aus Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="451bd-119">The following screen shot shows a core Tab from Windows 7 Paint.</span></span>

![Screenshot mit einem Registerkarten-Steuerelement.](images/controls/coretab.png)

## <a name="tab-properties"></a><span data-ttu-id="451bd-121">Registerkarteneigenschaften</span><span class="sxs-lookup"><span data-stu-id="451bd-121">Tab Properties</span></span>

<span data-ttu-id="451bd-122">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Registerkarten-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="451bd-122">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab control.</span></span>

<span data-ttu-id="451bd-123">In der Regel wird eine Registerkarten Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="451bd-123">Typically, a Tab property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="451bd-124">Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="451bd-124">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="451bd-125">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="451bd-125">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="451bd-126">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="451bd-126">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="451bd-127">In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="451bd-127">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="451bd-128">In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Registerkarten-Steuerelement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="451bd-128">The following table lists the property keys that are associated with the Tab control.</span></span>



| <span data-ttu-id="451bd-129">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="451bd-129">Property Key</span></span>                                                                                     | <span data-ttu-id="451bd-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="451bd-130">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="451bd-131">UI- \_ pkey- \_ Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="451bd-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="451bd-132">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="451bd-132">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="451bd-133">UI- \_ pkey- \_ KeyTip</span><span class="sxs-lookup"><span data-stu-id="451bd-133">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="451bd-134">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="451bd-134">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="451bd-135">UI- \_ pkey- \_ tooltipdescription</span><span class="sxs-lookup"><span data-stu-id="451bd-135">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="451bd-136">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="451bd-136">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="451bd-137">UI- \_ pkey- \_ ToolTipTitle</span><span class="sxs-lookup"><span data-stu-id="451bd-137">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="451bd-138">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="451bd-138">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="451bd-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="451bd-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="451bd-140">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="451bd-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="451bd-141">**Tab-Markup Element**</span><span class="sxs-lookup"><span data-stu-id="451bd-141">**Tab markup element**</span></span>](windowsribbon-element-tab.md)
</dt> </dl>

 

 
