---
title: Windows-Menüband-Steuerelement Bibliothek
description: In den Themen in diesem Abschnitt wird der Satz von Steuerelementen beschrieben, die im Windows-Menü Band Framework enthalten sind. Die hier aufgeführten Steuerelemente sind die UI-Objekte in einem Menüband, die Befehls Funktionalität verfügbar machen.
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840b07bafe0c43cb7ab148a4413657b9722c409b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341321"
---
# <a name="windows-ribbon-framework-control-library"></a><span data-ttu-id="23fbd-104">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="23fbd-104">Windows Ribbon Framework Control Library</span></span>

<span data-ttu-id="23fbd-105">In den Themen in diesem Abschnitt wird der Satz von Steuerelementen beschrieben, die im Windows-Menü Band Framework enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="23fbd-105">The topics contained in this section describe the set of controls that are included with the Windows Ribbon framework.</span></span> <span data-ttu-id="23fbd-106">Die hier aufgeführten Steuerelemente sind die UI-Objekte in einem Menüband, die Befehls Funktionalität verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="23fbd-106">The controls listed here are the UI objects in a ribbon that expose Command functionality.</span></span>

-   [<span data-ttu-id="23fbd-107">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="23fbd-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="23fbd-108">Die Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="23fbd-108">The Controls</span></span>](#windows-ribbon-framework-control-library)
    -   [<span data-ttu-id="23fbd-109">Grundlegende Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="23fbd-109">Basic Controls</span></span>](#basic-controls)
    -   [<span data-ttu-id="23fbd-110">Container Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="23fbd-110">Container Controls</span></span>](#container-controls)
    -   [<span data-ttu-id="23fbd-111">Spezialisierte Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="23fbd-111">Specialized Controls</span></span>](#specialized-controls)
-   [<span data-ttu-id="23fbd-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23fbd-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="23fbd-113">Einführung</span><span class="sxs-lookup"><span data-stu-id="23fbd-113">Introduction</span></span>

<span data-ttu-id="23fbd-114">Das Menüband-Framework besteht aus Komponenten wie [Registerkarten](windowsribbon-controls-tab.md) und der [Symbolleiste für den schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md), die zusammenarbeiten, um eine umfangreiche Benutzeroberfläche bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="23fbd-114">The Ribbon framework is composed of components such as [Tabs](windowsribbon-controls-tab.md) and the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md), that work together to deliver a rich UI experience.</span></span> <span data-ttu-id="23fbd-115">Diese Komponenten stellen verschiedene Arten von Befehlen zur Verfügung, um Kunden eine strukturierte, vorhersagbare Darstellung für multifunktionsleistenanwendungen zu bieten.</span><span class="sxs-lookup"><span data-stu-id="23fbd-115">Individually, these components expose different types of Commands to give customers an organized, predictable experience across Ribbon applications.</span></span> <span data-ttu-id="23fbd-116">Beispielsweise macht jede Registerkarte Befehle verfügbar, die sich auf das Erstellen und bearbeiten bestimmter Teile des Inhalts im Anwendungs Arbeitsbereich beziehen, während das [Anwendungsmenü](windowsribbon-controls-applicationmenu.md) Funktionen bereitstellt, die mit einem vollständigen Projekt verknüpft sind, z. b. ein gesamtes Dokument, Bild oder Film.</span><span class="sxs-lookup"><span data-stu-id="23fbd-116">For example, each Tab exposes Commands related to creating and acting on specific parts of the content within the application workspace, whereas the [Application Menu](windowsribbon-controls-applicationmenu.md) exposes functionality related to a complete project, such as an entire document, picture, or movie.</span></span>

<span data-ttu-id="23fbd-117">Dieses Thema enthält eine umfassende Liste der Menüband-Steuerelemente und enthält eine kurze Beschreibung der einzelnen Steuerelemente, mit Links zu ausführlicheren Dokumentationen, soweit verfügbar.</span><span class="sxs-lookup"><span data-stu-id="23fbd-117">This topic provides a comprehensive list of Ribbon controls and includes a brief description for each control, with links to more detailed documentation where available.</span></span>

## <a name="the-controls"></a><span data-ttu-id="23fbd-118">Die Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="23fbd-118">The Controls</span></span>

<span data-ttu-id="23fbd-119">Das Menüband-Framework besteht aus zwei [Ansichten](windowsribbon-reference-elements-view.md): der Menü [**Band**](windowsribbon-element-ribbon.md) Ansicht und der [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht.</span><span class="sxs-lookup"><span data-stu-id="23fbd-119">The Ribbon framework is composed of two [Views](windowsribbon-reference-elements-view.md): the [**Ribbon**](windowsribbon-element-ribbon.md) View and the [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span> <span data-ttu-id="23fbd-120">Jede Ansicht kann mehrere Komponenten hosten, die als Präsentations Container für alle Steuerelemente fungieren, die vom Framework gerendert und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="23fbd-120">Each View can host several components that act as presentation containers for all controls that are rendered and managed by the framework.</span></span>

<span data-ttu-id="23fbd-121">Die [**Menüband**](windowsribbon-element-ribbon.md) -Ansicht hostet das Element [**applicationmenu**](windowsribbon-element-applicationmenu.md) , das [**quickaccesstoolbar**](windowsribbon-element-quickaccesstoolbar.md) -Element und die Menüband-Befehlsleiste, während die [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht ein [**ContextMenu**](windowsribbon-element-contextmenu.md) -Element, ein [**MiniToolbar**](windowsribbon-element-minitoolbar.md) -Element oder beides hostet.</span><span class="sxs-lookup"><span data-stu-id="23fbd-121">The [**Ribbon**](windowsribbon-element-ribbon.md) View hosts the [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element, [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) element, and ribbon command bar while the [**ContextPopup**](windowsribbon-element-contextpopup.md) View hosts a [**ContextMenu**](windowsribbon-element-contextmenu.md) element, a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element, or both.</span></span>

<span data-ttu-id="23fbd-122">Jedes Framework-Steuerelement wird durch die Funktionalität unterschieden, die seinem [**Befehlstyp**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="23fbd-122">Each framework control is distinguished by the functionality associated with its [**Command type**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).</span></span>

### <a name="basic-controls"></a><span data-ttu-id="23fbd-123">Grundlegende Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="23fbd-123">Basic Controls</span></span>

<span data-ttu-id="23fbd-124">Grundlegende Steuerelemente bestehen aus einer oder mehreren Schaltflächen, die per Mausklick aufgerufen werden können, um eine einfache Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="23fbd-124">Basic controls consist of one or more buttons that can be invoked by a single mouse click to perform a simple action.</span></span>

> [!Note]  
> <span data-ttu-id="23fbd-125">Der [**Spinner**](windowsribbon-element-spinner.md) ist eine Ausnahme, da er ein Bearbeitungs Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="23fbd-125">The [**Spinner**](windowsribbon-element-spinner.md) is an exception as it contains an edit control.</span></span>

 

<span data-ttu-id="23fbd-126">In der folgenden Tabelle sind die grundlegenden Steuerelemente im Menüband-Framework aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="23fbd-126">The following table lists the basic controls in the Ribbon framework.</span></span>



| <span data-ttu-id="23fbd-127">Control</span><span class="sxs-lookup"><span data-stu-id="23fbd-127">Control</span></span>                                                  | <span data-ttu-id="23fbd-128">Markup-Element</span><span class="sxs-lookup"><span data-stu-id="23fbd-128">Markup Element</span></span>                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="23fbd-129">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="23fbd-129">Button</span></span>](windowsribbon-controls-button.md)              | [<span data-ttu-id="23fbd-130">**Gedrückt**</span><span class="sxs-lookup"><span data-stu-id="23fbd-130">**Button**</span></span>](windowsribbon-element-button.md)             |
| [<span data-ttu-id="23fbd-131">Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="23fbd-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)         | [<span data-ttu-id="23fbd-132">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="23fbd-132">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)         |
| [<span data-ttu-id="23fbd-133">Hilfe Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="23fbd-133">Help Button</span></span>](windowsribbon-controls-helpbutton.md)     | [<span data-ttu-id="23fbd-134">**HelpButton**</span><span class="sxs-lookup"><span data-stu-id="23fbd-134">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)     |
| [<span data-ttu-id="23fbd-135">Spinner</span><span class="sxs-lookup"><span data-stu-id="23fbd-135">Spinner</span></span>](windowsribbon-controls-spinner.md)            | [<span data-ttu-id="23fbd-136">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="23fbd-136">**Spinner**</span></span>](windowsribbon-element-spinner.md)           |
| [<span data-ttu-id="23fbd-137">UMSCHALT Fläche</span><span class="sxs-lookup"><span data-stu-id="23fbd-137">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md) | [<span data-ttu-id="23fbd-138">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="23fbd-138">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a><span data-ttu-id="23fbd-139">Container Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="23fbd-139">Container Controls</span></span>

<span data-ttu-id="23fbd-140">Container Steuerelemente bestehen aus Gruppen von Steuerelementen, Menüs, Listen oder Element-und Befehls Sammlungen.</span><span class="sxs-lookup"><span data-stu-id="23fbd-140">Container controls are composed of groups of controls, menus, lists, or item and Command collections.</span></span>

<span data-ttu-id="23fbd-141">Das Framework unterscheidet zwischen zwei Arten von Containern, statisch und dynamisch.</span><span class="sxs-lookup"><span data-stu-id="23fbd-141">The framework distinguishes between two types of containers, static and dynamic.</span></span>

### <a name="static-containers"></a><span data-ttu-id="23fbd-142">Statische Container</span><span class="sxs-lookup"><span data-stu-id="23fbd-142">Static Containers</span></span>

<span data-ttu-id="23fbd-143">Statische Container werden zusammen mit allen zugeordneten Ressourcen in der Menüband-Markup Datei deklariert und aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="23fbd-143">Static containers are declared and populated, along with all associated resources, in the Ribbon markup file.</span></span> <span data-ttu-id="23fbd-144">Diese Steuerelemente können zur Laufzeit nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="23fbd-144">These controls cannot be modified at run time.</span></span>

<span data-ttu-id="23fbd-145">Zu den Vorteilen statischer Steuerelemente gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="23fbd-145">The advantages of static controls include the following:</span></span>

-   <span data-ttu-id="23fbd-146">Schnelles Prototypen.</span><span class="sxs-lookup"><span data-stu-id="23fbd-146">Rapid prototyping.</span></span> <span data-ttu-id="23fbd-147">Statische Steuerelemente ermöglichen das schnelle Erstellen eines Menüband-Mock-up, das einem abschließenden Menüband-Design ähnelt, das keinen komplizierten Code erfordert.</span><span class="sxs-lookup"><span data-stu-id="23fbd-147">Static controls make it possible to quickly build a Ribbon mock-up resembling a final Ribbon design that requires no complicated code.</span></span>
-   <span data-ttu-id="23fbd-148">Einfache Änderungen.</span><span class="sxs-lookup"><span data-stu-id="23fbd-148">Easy modifications.</span></span> <span data-ttu-id="23fbd-149">Die meisten Elemente, Attribute, Ressourcen und Layouts statischer Steuerelemente können im Markup geändert werden.</span><span class="sxs-lookup"><span data-stu-id="23fbd-149">Most elements, attributes, resources, and layouts of static controls can be modified in markup.</span></span>
-   <span data-ttu-id="23fbd-150">Konsistente Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="23fbd-150">Consistent UI.</span></span> <span data-ttu-id="23fbd-151">Gut entworfene Anwendungen bieten eine konsistente und stabile Benutzeroberfläche, mit der Änderungen an Menüs und Listen zur Laufzeit vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="23fbd-151">Well-designed applications provide a consistent and stable UI that avoids changes to menus and lists at run time.</span></span>

<span data-ttu-id="23fbd-152">In der folgenden Tabelle werden die statischen Container-Steuerelemente im Menüband-Framework beschrieben.</span><span class="sxs-lookup"><span data-stu-id="23fbd-152">The following table describes the static container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="23fbd-153">Control</span><span class="sxs-lookup"><span data-stu-id="23fbd-153">Control</span></span>                                                        | <span data-ttu-id="23fbd-154">Markup-Element</span><span class="sxs-lookup"><span data-stu-id="23fbd-154">Markup Element</span></span>                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="23fbd-155">Anwendungsmenü</span><span class="sxs-lookup"><span data-stu-id="23fbd-155">Application Menu</span></span>](windowsribbon-controls-applicationmenu.md) | [<span data-ttu-id="23fbd-156">**Applicationmenu**</span><span class="sxs-lookup"><span data-stu-id="23fbd-156">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md) |
| [<span data-ttu-id="23fbd-157">Kontext-Popup</span><span class="sxs-lookup"><span data-stu-id="23fbd-157">Context Popup</span></span>](windowsribbon-controls-contextpopup.md)       | [<span data-ttu-id="23fbd-158">**Contextpopup**</span><span class="sxs-lookup"><span data-stu-id="23fbd-158">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)       |
| [<span data-ttu-id="23fbd-159">Dropdown Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="23fbd-159">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)  | [<span data-ttu-id="23fbd-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="23fbd-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)   |
| [<span data-ttu-id="23fbd-161">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="23fbd-161">Group</span></span>](windowsribbon-controls-group.md)                      | [<span data-ttu-id="23fbd-162">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="23fbd-162">**Group**</span></span>](windowsribbon-element-group.md)                     |
| [<span data-ttu-id="23fbd-163">Menü Gruppe</span><span class="sxs-lookup"><span data-stu-id="23fbd-163">Menu Group</span></span>](windowsribbon-controls-menugroup.md)             | [<span data-ttu-id="23fbd-164">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="23fbd-164">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)             |
| [<span data-ttu-id="23fbd-165">Trenn Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="23fbd-165">Split Button</span></span>](windowsribbon-controls-splitbutton.md)         | [<span data-ttu-id="23fbd-166">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="23fbd-166">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)         |
| [<span data-ttu-id="23fbd-167">TAB</span><span class="sxs-lookup"><span data-stu-id="23fbd-167">Tab</span></span>](windowsribbon-controls-tab.md)                          | [<span data-ttu-id="23fbd-168">**Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="23fbd-168">**Tab**</span></span>](windowsribbon-element-tab.md)                         |
| [<span data-ttu-id="23fbd-169">Registerkarten Gruppe</span><span class="sxs-lookup"><span data-stu-id="23fbd-169">Tab Group</span></span>](windowsribbon-controls-tabgroup.md)               | [<span data-ttu-id="23fbd-170">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="23fbd-170">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a><span data-ttu-id="23fbd-171">Dynamische Container</span><span class="sxs-lookup"><span data-stu-id="23fbd-171">Dynamic Containers</span></span>

<span data-ttu-id="23fbd-172">Dynamische Container werden in der Menüband-Markup Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="23fbd-172">Dynamic containers are declared in the Ribbon markup file.</span></span> <span data-ttu-id="23fbd-173">Sie verfügen über eine Gruppe von Elementen oder Befehlen, die zur Laufzeit erstellt oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="23fbd-173">They feature a group of items or Commands that are created or modified at run time.</span></span>

<span data-ttu-id="23fbd-174">Eine Unterklasse dynamischer Container, die als Galerien bezeichnet werden, unterscheidet sich durch ihre Implementierung der [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="23fbd-174">A subclass of dynamic containers, called galleries, are distinguished by their implementation of the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="23fbd-175">Diese Schnittstelle ermöglicht es einem Steuerelement, seine Elemente oder Befehlsliste als Auflistung verfügbar zu machen und Aktualisierungen auf der Grundlage der Benutzerinteraktion und der Lauf Zeit Bedingungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="23fbd-175">This interface allows a control to expose its item or Command list as a collection, and to support updates based on both user interaction and run-time conditions.</span></span> <span data-ttu-id="23fbd-176">Weitere Informationen finden Sie unter [Arbeiten mit Galerien](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="23fbd-176">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="23fbd-177">In der folgenden Tabelle werden die dynamischen Container Steuerelemente im Menüband-Framework aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="23fbd-177">The following table lists the dynamic container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="23fbd-178">Control</span><span class="sxs-lookup"><span data-stu-id="23fbd-178">Control</span></span>                                                               | <span data-ttu-id="23fbd-179">Markup-Element</span><span class="sxs-lookup"><span data-stu-id="23fbd-179">Markup Element</span></span>                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="23fbd-180">Kombinations Feld</span><span class="sxs-lookup"><span data-stu-id="23fbd-180">Combo Box</span></span>](windowsribbon-controls-combobox.md)                      | [<span data-ttu-id="23fbd-181">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="23fbd-181">**ComboBox**</span></span>](windowsribbon-element-combobox.md)                     |
| [<span data-ttu-id="23fbd-182">Dropdown-Katalog</span><span class="sxs-lookup"><span data-stu-id="23fbd-182">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)       | [<span data-ttu-id="23fbd-183">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="23fbd-183">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       |
| [<span data-ttu-id="23fbd-184">In-Ribbon-Katalog</span><span class="sxs-lookup"><span data-stu-id="23fbd-184">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)       | [<span data-ttu-id="23fbd-185">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="23fbd-185">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       |
| [<span data-ttu-id="23fbd-186">Symbolleiste für den Schnellzugriff</span><span class="sxs-lookup"><span data-stu-id="23fbd-186">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md) | [<span data-ttu-id="23fbd-187">**Quickaccesstoolbar**</span><span class="sxs-lookup"><span data-stu-id="23fbd-187">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md) |
| [<span data-ttu-id="23fbd-188">Zuletzt verwendete Elemente</span><span class="sxs-lookup"><span data-stu-id="23fbd-188">Recent Items</span></span>](windowsribbon-controls-recentitems.md)                | [<span data-ttu-id="23fbd-189">**"Recentitems"**</span><span class="sxs-lookup"><span data-stu-id="23fbd-189">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)               |
| [<span data-ttu-id="23fbd-190">Split Button-Katalog</span><span class="sxs-lookup"><span data-stu-id="23fbd-190">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md) | [<span data-ttu-id="23fbd-191">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="23fbd-191">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a><span data-ttu-id="23fbd-192">Spezialisierte Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="23fbd-192">Specialized Controls</span></span>

<span data-ttu-id="23fbd-193">Das Menüband-Framework enthält eine Reihe spezieller Steuerelemente für bestimmte UI-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="23fbd-193">The Ribbon framework contains a number of specialized controls for specific UI functionality.</span></span>

<span data-ttu-id="23fbd-194">In der folgenden Tabelle sind die spezialisierten Steuerelemente im Menüband-Framework aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="23fbd-194">The following table lists the specialized controls in the Ribbon framework.</span></span>



| <span data-ttu-id="23fbd-195">Control</span><span class="sxs-lookup"><span data-stu-id="23fbd-195">Control</span></span>                                                                  | <span data-ttu-id="23fbd-196">Markup-Element</span><span class="sxs-lookup"><span data-stu-id="23fbd-196">Markup Element</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="23fbd-197">Dropdown-Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="23fbd-197">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | [<span data-ttu-id="23fbd-198">**Dropdowncolorpicker**</span><span class="sxs-lookup"><span data-stu-id="23fbd-198">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md) |
| [<span data-ttu-id="23fbd-199">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="23fbd-199">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | [<span data-ttu-id="23fbd-200">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="23fbd-200">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="23fbd-201">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23fbd-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23fbd-202">Grundlegendes zu Befehlen und Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="23fbd-202">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 