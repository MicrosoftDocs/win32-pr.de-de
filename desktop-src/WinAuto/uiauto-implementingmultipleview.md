---
title: MultipleView-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IMultipleViewProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des MultipleView-Steuerelement Musters
- UI-Automatisierung, MultipleView-Steuerelement Muster
- UI-Automatisierung, IMultipleViewProvider
- IMultipleViewProvider
- Implementieren von MultipleView-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- MultipleView-Steuerelement Muster
- Steuerelement Muster, IMultipleViewProvider
- Steuerelement Muster, Implementieren der UI-Automatisierung MultipleView
- Steuerelement Muster, MultipleView
- Schnittstellen, IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388452"
---
# <a name="multipleview-control-pattern"></a><span data-ttu-id="a4f5f-113">MultipleView-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="a4f5f-113">MultipleView Control Pattern</span></span>

<span data-ttu-id="a4f5f-114">Beschreibt Richtlinien und Konventionen für das Implementieren von [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="a4f5f-114">Describes guidelines and conventions for implementing [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), including information about properties and methods.</span></span> <span data-ttu-id="a4f5f-115">Links zu zusätzlichen Referenzen sind am Ende dieses Themas aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a4f5f-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="a4f5f-116">Das **MultipleView** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die mehrere Darstellungen derselben Informationen oder desselben Satzes von untergeordneten Steuerelementen bereitstellen und zwischen diesen wechseln können.</span><span class="sxs-lookup"><span data-stu-id="a4f5f-116">The **MultipleView** control pattern is used to support controls that provide, and are able to switch between, multiple representations of the same information or the same set of child controls.</span></span>

<span data-ttu-id="a4f5f-117">Beispiele für Steuerelemente, die mehrere Ansichten darstellen können, sind die Listenansicht (die den Inhalt als Miniaturansichten anzeigen kann. Kacheln, Symbole oder Details), Microsoft Excel-Diagramme (Kreis-, Linien-, Balken-, Zellwert mit einer Formel), Microsoft Word-Dokumente (normal, Weblayout, Drucklayout, Lese Layout, Gliederung), Microsoft Outlook-Kalender (Jahr, Monat, Woche, Tag) und Microsoft Windows Media Player Skins.</span><span class="sxs-lookup"><span data-stu-id="a4f5f-117">Examples of controls that can present multiple views include the list view (which can show its contents as thumbnails, tiles, icons, or details), Microsoft Excel charts (pie, line, bar, cell value with a formula), Microsoft Word documents (normal, web layout, print layout, reading layout, outline), Microsoft Outlook calendar (year, month, week, day), and Microsoft Windows Media Player skins.</span></span> <span data-ttu-id="a4f5f-118">Die unterstützten Ansichten werden vom Steuerelemententwickler bestimmt und sind für jedes Steuerelement spezifisch.</span><span class="sxs-lookup"><span data-stu-id="a4f5f-118">The supported views are determined by the control developer and are specific to each control.</span></span>

<span data-ttu-id="a4f5f-119">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="a4f5f-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a4f5f-120">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="a4f5f-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="a4f5f-121">Erforderliche Member für **IMultipleViewProvider**</span><span class="sxs-lookup"><span data-stu-id="a4f5f-121">Required Members for **IMultipleViewProvider**</span></span>](#required-members-for-imultipleviewprovider)
-   [<span data-ttu-id="a4f5f-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4f5f-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="a4f5f-123">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="a4f5f-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="a4f5f-124">Beachten Sie beim Implementieren des **MultipleView** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="a4f5f-124">When implementing the **MultipleView** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="a4f5f-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) sollte auch für einen Container implementiert werden, der die aktuelle Ansicht verwaltet, wenn Sie sich von einem Steuerelement unterscheidet, das die aktuelle Ansicht bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a4f5f-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) should also be implemented on a container that manages the current view if it is different from a control that provides the current view.</span></span> <span data-ttu-id="a4f5f-126">Windows-Explorer enthält z. b. ein Listen Steuerelement für den aktuellen Ordner Inhalt, während die Ansicht für das Steuerelement über die Windows Explorer-Anwendung verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="a4f5f-126">For example, Windows Explorer contains a list control for the current folder content while the view for the control is managed from the Windows Explorer application.</span></span>
-   <span data-ttu-id="a4f5f-127">Ein Steuerelement, das seinen Inhalt sortieren kann, wird nicht als Steuerelement betrachtet, das mehrere Ansichten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a4f5f-127">A control that is able to sort its content is not considered to support multiple views.</span></span>
-   <span data-ttu-id="a4f5f-128">Die Auflistung von Ansichten muss instanzenübergreifend identisch sein.</span><span class="sxs-lookup"><span data-stu-id="a4f5f-128">The collection of views must be identical across instances.</span></span>
-   <span data-ttu-id="a4f5f-129">Ansichts Namen müssen für Text-zu-Sprache, Braille und andere lesbare Anwendungen geeignet sein.</span><span class="sxs-lookup"><span data-stu-id="a4f5f-129">View names must be suitable for use in text to speech, Braille, and other human-readable applications.</span></span>

## <a name="required-members-for-imultipleviewprovider"></a><span data-ttu-id="a4f5f-130">Erforderliche Member für **IMultipleViewProvider**</span><span class="sxs-lookup"><span data-stu-id="a4f5f-130">Required Members for **IMultipleViewProvider**</span></span>

<span data-ttu-id="a4f5f-131">Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a4f5f-131">The following properties and methods are required for implementing the [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) interface.</span></span>



| <span data-ttu-id="a4f5f-132">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="a4f5f-132">Required members</span></span>                                                            | <span data-ttu-id="a4f5f-133">Memberart</span><span class="sxs-lookup"><span data-stu-id="a4f5f-133">Member type</span></span> | <span data-ttu-id="a4f5f-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a4f5f-134">Notes</span></span> |
|-----------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="a4f5f-135">**CurrentView**</span><span class="sxs-lookup"><span data-stu-id="a4f5f-135">**CurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | <span data-ttu-id="a4f5f-136">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4f5f-136">Property</span></span>    | <span data-ttu-id="a4f5f-137">Keine</span><span class="sxs-lookup"><span data-stu-id="a4f5f-137">None</span></span>  |
| [<span data-ttu-id="a4f5f-138">**GetSupportedViews**</span><span class="sxs-lookup"><span data-stu-id="a4f5f-138">**GetSupportedViews**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | <span data-ttu-id="a4f5f-139">Methode</span><span class="sxs-lookup"><span data-stu-id="a4f5f-139">Method</span></span>      | <span data-ttu-id="a4f5f-140">Keine</span><span class="sxs-lookup"><span data-stu-id="a4f5f-140">None</span></span>  |
| [<span data-ttu-id="a4f5f-141">**GetViewName**</span><span class="sxs-lookup"><span data-stu-id="a4f5f-141">**GetViewName**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | <span data-ttu-id="a4f5f-142">Methode</span><span class="sxs-lookup"><span data-stu-id="a4f5f-142">Method</span></span>      | <span data-ttu-id="a4f5f-143">Keine</span><span class="sxs-lookup"><span data-stu-id="a4f5f-143">None</span></span>  |
| [<span data-ttu-id="a4f5f-144">**SetCurrentView**</span><span class="sxs-lookup"><span data-stu-id="a4f5f-144">**SetCurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | <span data-ttu-id="a4f5f-145">Methode</span><span class="sxs-lookup"><span data-stu-id="a4f5f-145">Method</span></span>      | <span data-ttu-id="a4f5f-146">Keine</span><span class="sxs-lookup"><span data-stu-id="a4f5f-146">None</span></span>  |



 

<span data-ttu-id="a4f5f-147">Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a4f5f-147">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4f5f-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4f5f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4f5f-149">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="a4f5f-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="a4f5f-150">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="a4f5f-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="a4f5f-151">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="a4f5f-151">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="a4f5f-152">ExpandCollapse-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="a4f5f-152">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




