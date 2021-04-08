---
title: Auswahl Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ISelectionProvider, einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Auswahl Steuerelement Musters
- UI-Automatisierung, Auswahl Steuerelement Muster
- UI-Automatisierung, ISelectionProvider
- ISelectionProvider
- Implementieren von Auswahl Steuerelement Mustern für Benutzeroberflächen Automatisierung
- Auswahl Steuerelement Muster
- Steuerelement Muster, ISelectionProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-Auswahl
- Steuerelement Muster, Auswahl
- Schnittstellen, ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037021"
---
# <a name="selection-control-pattern"></a><span data-ttu-id="c1f09-113">Auswahl Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="c1f09-113">Selection Control Pattern</span></span>

<span data-ttu-id="c1f09-114">Beschreibt Richtlinien und Konventionen für das Implementieren von [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="c1f09-114">Describes guidelines and conventions for implementing [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="c1f09-115">Das **Auswahl** Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die als Container für eine Auflistung von auswählbaren untergeordneten Elementen fungieren.</span><span class="sxs-lookup"><span data-stu-id="c1f09-115">The **Selection** control pattern is used to support controls that act as containers for a collection of selectable child items.</span></span> <span data-ttu-id="c1f09-116">Die untergeordneten Elemente dieses Elements müssen [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)implementieren.</span><span class="sxs-lookup"><span data-stu-id="c1f09-116">The children of this element must implement [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

<span data-ttu-id="c1f09-117">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="c1f09-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="c1f09-118">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="c1f09-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c1f09-119">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="c1f09-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="c1f09-120">Erforderliche Member für **ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="c1f09-120">Required Members for **ISelectionProvider**</span></span>](#required-members-for-iselectionprovider)
-   [<span data-ttu-id="c1f09-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1f09-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="c1f09-122">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="c1f09-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="c1f09-123">Beachten Sie beim Implementieren des **Selection** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="c1f09-123">When implementing the **Selection** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="c1f09-124">Bei Steuerelementen, die [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) implementieren, kann entweder ein oder mehrere untergeordnete Elemente ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="c1f09-124">Controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) allow either single or multiple child items to be selected.</span></span> <span data-ttu-id="c1f09-125">Listenfelder, Listenansichten und Struktur Ansichten unterstützen z. b. Mehrfachauswahl, während Kombinations Felder, Schieberegler und Optionsfeld Gruppen die einfache Auswahl unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c1f09-125">For example, list boxes, list views, and tree views support multiple selections, whereas combo boxes, sliders, and radio button groups support single selection.</span></span>
-   <span data-ttu-id="c1f09-126">Steuerelemente, die einen minimalen, maximalen und kontinuierlichen Bereich aufweisen, wie z. b. das **Volume** Slider-Steuerelement eines Media Players, sollten [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) anstelle von [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)implementieren.</span><span class="sxs-lookup"><span data-stu-id="c1f09-126">Controls that have a minimum, maximum, and continuous range, such as the **Volume** slider control of a media player, should implement [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) instead of [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>
-   <span data-ttu-id="c1f09-127">Steuerelemente mit einfacher Auswahl, die untergeordnete Steuerelemente verwalten, die [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)implementieren, z. b. den Schieberegler **Bildschirmauflösung** im Dialogfeld **Anzeigeeigenschaften** für Windows oder das **Farb** Auswahl-Auswahl Steuerelement von Microsoft Word (siehe folgende Abbildung), sollte [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); implementieren. die untergeordneten Elemente sollten sowohl " [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) " als auch " [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)" implementieren.</span><span class="sxs-lookup"><span data-stu-id="c1f09-127">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, or the **Color Picker** selection control from Microsoft Word (see the following image), should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

    ![Bild mit einem Beispiel für Zeichen folgen Zuordnung von Farbmustern](images/uia-valuepattern-colorpicker.jpg)

-   <span data-ttu-id="c1f09-129">Menüs unterstützen das **Auswahl** Steuerelement Muster nicht.</span><span class="sxs-lookup"><span data-stu-id="c1f09-129">Menus do not support the **Selection** control pattern.</span></span> <span data-ttu-id="c1f09-130">Wenn Sie mit Menü Elementen arbeiten, die Grafiken und Text enthalten (z. b. die Elemente im **Vorschau** Bereich im Menü **Ansicht** in Microsoft Outlook) und den Zustand übermitteln müssen, sollten Sie [**ideggleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)implementieren.</span><span class="sxs-lookup"><span data-stu-id="c1f09-130">If you are working with menu items that include both graphics and text (such as the **Preview Pane** items in the **View** menu in Microsoft Outlook) and need to convey state, you should implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span></span>

## <a name="required-members-for-iselectionprovider"></a><span data-ttu-id="c1f09-131">Erforderliche Member für **ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="c1f09-131">Required Members for **ISelectionProvider**</span></span>

<span data-ttu-id="c1f09-132">Die folgenden Eigenschaften, Methoden und Ereignisse sind für die Implementierung der [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c1f09-132">The following properties, methods, and events are required for implementing the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>



| <span data-ttu-id="c1f09-133">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="c1f09-133">Required members</span></span>                                                                                | <span data-ttu-id="c1f09-134">Memberart</span><span class="sxs-lookup"><span data-stu-id="c1f09-134">Member type</span></span> | <span data-ttu-id="c1f09-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1f09-135">Notes</span></span>                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="c1f09-136">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="c1f09-136">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | <span data-ttu-id="c1f09-137">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c1f09-137">Property</span></span>    | <span data-ttu-id="c1f09-138">Keine</span><span class="sxs-lookup"><span data-stu-id="c1f09-138">None</span></span>                                                                        |
| [<span data-ttu-id="c1f09-139">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="c1f09-139">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | <span data-ttu-id="c1f09-140">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c1f09-140">Property</span></span>    | <span data-ttu-id="c1f09-141">Keine</span><span class="sxs-lookup"><span data-stu-id="c1f09-141">None</span></span>                                                                        |
| [<span data-ttu-id="c1f09-142">**GetSelection**</span><span class="sxs-lookup"><span data-stu-id="c1f09-142">**GetSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | <span data-ttu-id="c1f09-143">Methode</span><span class="sxs-lookup"><span data-stu-id="c1f09-143">Method</span></span>      | <span data-ttu-id="c1f09-144">Keine</span><span class="sxs-lookup"><span data-stu-id="c1f09-144">None</span></span>                                                                        |
| [<span data-ttu-id="c1f09-145">**UIA- \_ Auswahl \_ invalidatedeventid**</span><span class="sxs-lookup"><span data-stu-id="c1f09-145">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="c1f09-146">Ereignis</span><span class="sxs-lookup"><span data-stu-id="c1f09-146">Event</span></span>       | <span data-ttu-id="c1f09-147">Dieses Ereignis wird durch eine deutliche Änderung einer Auswahl in einem Container angehoben.</span><span class="sxs-lookup"><span data-stu-id="c1f09-147">Raise this event when a selection in a container has changed significantly.</span></span> |



 

<span data-ttu-id="c1f09-148">Die Eigenschaften " [**ISelectionProvider:: IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) " und " [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) " können dynamisch sein.</span><span class="sxs-lookup"><span data-stu-id="c1f09-148">The [**ISelectionProvider::IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) and [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) properties can be dynamic.</span></span> <span data-ttu-id="c1f09-149">Beispielsweise können für den ursprünglichen Zustand eines Steuer Elements keine Elemente standardmäßig ausgewählt werden, was darauf hinweist, dass **IsSelectionRequired** false ist.</span><span class="sxs-lookup"><span data-stu-id="c1f09-149">For example, the initial state of a control might not have any items selected by default, indicating that **IsSelectionRequired** is false.</span></span> <span data-ttu-id="c1f09-150">Nach dem Auswählen eines Elements muss für das Steuerelement jedoch immer mindestens ein Element ausgewählt sein.</span><span class="sxs-lookup"><span data-stu-id="c1f09-150">However, after an item is selected, the control must always have at least one item selected.</span></span> <span data-ttu-id="c1f09-151">Auf ähnliche Weise kann ein Steuerelement in seltenen Fällen bei der Initialisierung die Mehrfachauswahl von Elementen gestatten, während anschließend nur noch die Einfachauswahl zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="c1f09-151">Similarly, in rare cases, a control might allow multiple items to be selected on initialization, but subsequently allow only single selections to be made.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1f09-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1f09-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1f09-153">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="c1f09-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="c1f09-154">SelectionItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="c1f09-154">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
</dt> <dt>

[<span data-ttu-id="c1f09-155">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="c1f09-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="c1f09-156">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="c1f09-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




