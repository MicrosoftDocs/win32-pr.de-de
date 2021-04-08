---
title: Arbeiten mit Galerien
description: Das Windows-Menü Band Framework bietet Entwicklern ein stabiles und konsistentes Modell für die Verwaltung dynamischer Inhalte über eine Vielzahl von Sammlungs basierten Steuerelementen.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Windows-Menüband, Galerien
- Menüband, Galerien
- Windows-Menüband, dropdowngallery-Steuerelement
- Menüband, dropdowngallery-Steuerelement
- Windows-Menüband, splitbuttongallery-Steuerelement
- Multifunktionsleiste, splitbuttongallery-Steuerelement
- Dropdowngallery-Steuerelement
- Splitbuttongallery-Steuerelement
- Menüband für Windows-Kataloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784c69b0cf23edad906fbb35ee9a2a45454eacea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729232"
---
# <a name="working-with-galleries"></a><span data-ttu-id="f52e3-112">Arbeiten mit Galerien</span><span class="sxs-lookup"><span data-stu-id="f52e3-112">Working with Galleries</span></span>

<span data-ttu-id="f52e3-113">Das Windows-Menü Band Framework bietet Entwicklern ein stabiles und konsistentes Modell für die Verwaltung dynamischer Inhalte über eine Vielzahl von Sammlungs basierten Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="f52e3-113">The Windows Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="f52e3-114">Durch das anpassen und Neukonfigurieren der Multifunktionsleisten-Benutzeroberfläche ermöglichen diese dynamischen Steuerelemente dem Framework die Reaktion auf Benutzerinteraktionen sowohl in der Host Anwendung als auch auf dem Menüband selbst und bieten die Flexibilität, verschiedene Laufzeitumgebungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f52e3-114">By adapting and reconfiguring the Ribbon UI, these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

-   [<span data-ttu-id="f52e3-115">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="f52e3-115">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="f52e3-116">Buden</span><span class="sxs-lookup"><span data-stu-id="f52e3-116">Galleries</span></span>](#working-with-galleries)
    -   [<span data-ttu-id="f52e3-117">Element Kataloge</span><span class="sxs-lookup"><span data-stu-id="f52e3-117">Item Galleries</span></span>](#item-galleries)
    -   [<span data-ttu-id="f52e3-118">Befehls Galerien</span><span class="sxs-lookup"><span data-stu-id="f52e3-118">Command Galleries</span></span>](#command-galleries)
    -   [<span data-ttu-id="f52e3-119">Katalog Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="f52e3-119">Gallery Controls</span></span>](#working-with-galleries)
-   [<span data-ttu-id="f52e3-120">Vorgehensweise beim Implementieren eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="f52e3-120">How to Implement a Gallery</span></span>](#how-to-implement-a-gallery)
    -   [<span data-ttu-id="f52e3-121">Die grundlegenden Komponenten</span><span class="sxs-lookup"><span data-stu-id="f52e3-121">The Basic Components</span></span>](#the-basic-components)
    -   [<span data-ttu-id="f52e3-122">Deklarieren der Steuerelemente im Markup</span><span class="sxs-lookup"><span data-stu-id="f52e3-122">Declare the Controls in Markup</span></span>](#declare-the-controls-in-markup)
    -   [<span data-ttu-id="f52e3-123">Erstellen eines Befehls Handlers</span><span class="sxs-lookup"><span data-stu-id="f52e3-123">Create a Command Handler</span></span>](#create-a-command-handler)
    -   [<span data-ttu-id="f52e3-124">Binden des Befehls Handlers</span><span class="sxs-lookup"><span data-stu-id="f52e3-124">Bind the Command Handler</span></span>](#bind-the-command-handler)
    -   [<span data-ttu-id="f52e3-125">Initialisieren einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="f52e3-125">Initialize a Collection</span></span>](#initialize-a-collection)
    -   [<span data-ttu-id="f52e3-126">Behandeln von Sammlungs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f52e3-126">Handle Collection Events</span></span>](#handle-collection-events)
-   [<span data-ttu-id="f52e3-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f52e3-127">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="f52e3-128">Einführung</span><span class="sxs-lookup"><span data-stu-id="f52e3-128">Introduction</span></span>

<span data-ttu-id="f52e3-129">Diese Fähigkeit des Multifunktionsleisten-Frameworks, sich dynamisch an Lauf Zeit Bedingungen, Anwendungsanforderungen und Endbenutzer Eingaben anzupassen, hebt die umfassenden Benutzeroberflächen Funktionen des Frameworks hervor und bietet Entwicklern die Flexibilität, eine breite Palette von Kundenanforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="f52e3-129">This ability of the Ribbon framework to dynamically adapt to run-time conditions, application requirements, and end-user input highlights the rich UI capabilities of the framework, and provides developers with the flexibility to cater to a broad range of customer needs.</span></span>

<span data-ttu-id="f52e3-130">Der Schwerpunkt dieses Handbuchs besteht darin, die dynamischen Katalog Steuerelemente zu beschreiben, die vom Framework unterstützt werden, ihre Unterschiede zu erläutern, zu erörtern, wann und wo Sie am besten verwendet werden können, und zu veranschaulichen, wie Sie in eine Menü Bandanwendung integriert werden können</span><span class="sxs-lookup"><span data-stu-id="f52e3-130">The focus of this guide is to describe the dynamic gallery controls supported by the framework, explain their differences, discuss when and where they may best be used, and demonstrate how they can be incorporated into a Ribbon application.</span></span>

## <a name="galleries"></a><span data-ttu-id="f52e3-131">Kataloge</span><span class="sxs-lookup"><span data-stu-id="f52e3-131">Galleries</span></span>

<span data-ttu-id="f52e3-132">Galerien sind funktionale und grafisch umfangreiche Listenfeld-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="f52e3-132">Galleries are functionally and graphically rich list box controls.</span></span> <span data-ttu-id="f52e3-133">Die Element Auflistung eines Katalogs kann nach Kategorien organisiert werden, die in flexiblen Spalten-und Zeilen basierten Layouts angezeigt werden, die mit Bildern und Text dargestellt werden. abhängig vom Typ des Katalogs wird die Live Vorschau unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f52e3-133">The item collection of a gallery can be organized by categories, displayed in flexible column and row-based layouts, represented with images and text, and depending on the type of gallery, support live previewing.</span></span>

<span data-ttu-id="f52e3-134">Kataloge sind aus folgenden Gründen funktionell von anderen dynamischen Menüband-Steuerelementen unterschieden:</span><span class="sxs-lookup"><span data-stu-id="f52e3-134">Galleries are functionally distinct from other dynamic Ribbon controls for the following reasons:</span></span>

-   <span data-ttu-id="f52e3-135">Kataloge implementieren die [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Schnittstelle, die die verschiedenen Methoden zum Bearbeiten von Galerie Element Auflistungen definiert.</span><span class="sxs-lookup"><span data-stu-id="f52e3-135">Galleries implement the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface that defines the various methods for manipulating gallery item collections.</span></span>
-   <span data-ttu-id="f52e3-136">Kataloge können zur Laufzeit auf der Grundlage von Aktivitäten aktualisiert werden, die direkt im Menüband auftreten, z. b. Wenn ein Benutzer der Symbolleiste für den schnell Zugriff (QAT) einen Befehl hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="f52e3-136">Galleries can be updated at run time, based on activity that occurs directly in the Ribbon, such as when a user adds a Command to the Quick Access Toolbar (QAT).</span></span>
-   <span data-ttu-id="f52e3-137">Kataloge können zur Laufzeit aktualisiert werden, basierend auf Aktivitäten, die indirekt aus der Laufzeitumgebung auftreten, z. b. Wenn ein Druckertreiber nur Hochformat Layouts unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f52e3-137">Galleries can be updated at run time, based on activity that occurs indirectly from the run-time environment, such as when a printer driver supports portrait page layouts only.</span></span>
-   <span data-ttu-id="f52e3-138">Kataloge können zur Laufzeit aktualisiert werden, basierend auf Aktivitäten, die indirekt in der Host Anwendung auftreten, z. b. Wenn ein Benutzer ein Element in einem Dokument auswählt.</span><span class="sxs-lookup"><span data-stu-id="f52e3-138">Galleries can be updated at run time, based on activity that occurs indirectly in the host application, such as when a user selects an item in a document.</span></span>

<span data-ttu-id="f52e3-139">Das Menüband-Framework macht zwei Arten von Galerien verfügbar: Element Kataloge und Befehls Galerien.</span><span class="sxs-lookup"><span data-stu-id="f52e3-139">The Ribbon framework exposes two types of galleries: item galleries and Command galleries.</span></span>

### <a name="item-galleries"></a><span data-ttu-id="f52e3-140">Element Kataloge</span><span class="sxs-lookup"><span data-stu-id="f52e3-140">Item Galleries</span></span>

<span data-ttu-id="f52e3-141">Element Kataloge enthalten eine indexbasierte Auflistung verwandter Elemente, wobei jedes Element durch ein Bild, eine Zeichenfolge oder beides dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f52e3-141">Item galleries contain an index-based collection of related items where each item is represented by an image, a string, or both.</span></span> <span data-ttu-id="f52e3-142">Das-Steuerelement ist an einen einzelnen Befehls Handler gebunden, der auf dem Indexwert basiert, der von der Benutzeroberflächen- [ \_ pkey \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) -Eigenschaft identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f52e3-142">The control is bound to a single Command handler that relies on the index value that is identified by the [UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) property.</span></span>

<span data-ttu-id="f52e3-143">Element Kataloge unterstützen die Live Vorschau. Dies bedeutet, dass ein Befehls Ergebnis basierend auf mouseover oder Fokus angezeigt wird, ohne dass ein Commit für den Befehl ausgeführt oder tatsächlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f52e3-143">Item galleries support live previewing, which means displaying a Command result, based on mouseover or focus, without committing to or actually invoking the Command.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f52e3-144">Das Framework bietet keine Unterstützung für das Hosting von Element Galerien im Anwendungsmenü.</span><span class="sxs-lookup"><span data-stu-id="f52e3-144">The framework does not support hosting item galleries in the Application Menu.</span></span>

 

### <a name="command-galleries"></a><span data-ttu-id="f52e3-145">Befehls Galerien</span><span class="sxs-lookup"><span data-stu-id="f52e3-145">Command Galleries</span></span>

<span data-ttu-id="f52e3-146">Befehls Galerien enthalten eine Auflistung von eindeutigen, nicht indizierten Elementen.</span><span class="sxs-lookup"><span data-stu-id="f52e3-146">Command galleries contain a collection of distinct, non-indexed items.</span></span> <span data-ttu-id="f52e3-147">Jedes Element wird durch ein einzelnes Steuerelement dargestellt, das über eine Befehls-ID an einen Befehls Handler gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="f52e3-147">Each item is represented by a single control bound to a Command handler through a Command ID.</span></span> <span data-ttu-id="f52e3-148">Ebenso wie eigenständige Steuerelemente leitet jedes Element in einer Befehls Galerie Eingabeereignisse an einen zugeordneten Befehls Handler weiter – die Befehls Galerie selbst lauscht nicht auf Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="f52e3-148">Like standalone controls, each item in a Command gallery routes input events to an associated Command handler—the Command gallery itself does not listen for events.</span></span>

<span data-ttu-id="f52e3-149">Befehls Galerien unterstützen keine Live Vorschau.</span><span class="sxs-lookup"><span data-stu-id="f52e3-149">Command galleries do not support live previewing.</span></span>

### <a name="gallery-controls"></a><span data-ttu-id="f52e3-150">Katalog Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="f52e3-150">Gallery Controls</span></span>

<span data-ttu-id="f52e3-151">Es gibt vier Katalog Steuerelemente im Menüband-Framework: [**dropdowngallery**](windowsribbon-element-dropdowngallery.md), [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md), [**inribbongallery**](windowsribbon-element-inribbongallery.md)und [**ComboBox**](windowsribbon-element-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="f52e3-151">There are four gallery controls in the Ribbon framework: the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), and the [**ComboBox**](windowsribbon-element-combobox.md).</span></span> <span data-ttu-id="f52e3-152">Alle außer **ComboBox** können entweder als Element Katalog oder als Befehls Katalog implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-152">All except the **ComboBox** can be implemented as either an item gallery or a Command gallery.</span></span>

### <a name="dropdowngallery"></a><span data-ttu-id="f52e3-153">Dropdown Gallery</span><span class="sxs-lookup"><span data-stu-id="f52e3-153">DropDownGallery</span></span>

<span data-ttu-id="f52e3-154">Ein [**dropdowngallery**](windowsribbon-element-dropdowngallery.md) ist eine Schaltfläche, die eine Dropdown Liste anzeigt, die eine Auflistung von sich gegenseitig ausschließenden Elementen oder Befehlen enthält.</span><span class="sxs-lookup"><span data-stu-id="f52e3-154">A [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) is a button that displays a drop-down list that contains a collection of mutually exclusive items or Commands.</span></span>

<span data-ttu-id="f52e3-155">Der folgende Screenshot veranschaulicht das Menüband [-Dropdown-](windowsribbon-controls-dropdowngallery.md) Katalog Steuerelement in Microsoft Paint für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f52e3-155">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot eines Dropdown Galerie-Steuer Elements in Microsoft Paint für Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a><span data-ttu-id="f52e3-157">Splitbuttongallery</span><span class="sxs-lookup"><span data-stu-id="f52e3-157">SplitButtonGallery</span></span>

<span data-ttu-id="f52e3-158">Ein [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) ist ein zusammengesetztes Steuerelement, das ein einzelnes Standardelement oder einen einzelnen Befehl aus seiner Auflistung auf einer primären Schaltfläche verfügbar macht und andere Elemente oder Befehle in einer sich gegenseitig ausschließenden Dropdown Liste anzeigt, die angezeigt wird, wenn auf eine sekundäre Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="f52e3-158">A [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) is a composite control that exposes a single default item or Command from its collection on a primary button, and displays other items or commands in a mutually exclusive drop-down list that is displayed when a secondary button is clicked.</span></span>

<span data-ttu-id="f52e3-159">Der folgende Screenshot veranschaulicht das Steuerelement für den [Menüband-unterteilte Schalt](windowsribbon-controls-splitbuttongallery.md) Flächen Katalog in Microsoft Paint für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f52e3-159">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot eines Steuer Elements für eine unterteilte Schaltflächen Galerie in Microsoft Paint für Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a><span data-ttu-id="f52e3-161">Inribbongallery</span><span class="sxs-lookup"><span data-stu-id="f52e3-161">InRibbonGallery</span></span>

<span data-ttu-id="f52e3-162">Ein [**inribbongallery**](windowsribbon-element-inribbongallery.md) -Katalog ist ein Katalog, in dem eine Sammlung verwandter Elemente oder Befehle im Menüband angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f52e3-162">An [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is a gallery that displays a collection of related items or Commands in the Ribbon.</span></span> <span data-ttu-id="f52e3-163">Wenn im Katalog zu viele Elemente vorhanden sind, wird ein Erweiterungs Pfeil bereitgestellt, um den Rest der Auflistung in einem erweiterten Bereich anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f52e3-163">If there are too many items in the gallery, an expand arrow is provided to display the rest of the collection in an expanded pane.</span></span>

<span data-ttu-id="f52e3-164">Der folgende Screenshot veranschaulicht das Multifunktionsleisten [-Steuerelement im Menüband-](windowsribbon-controls-inribbongallery.md) Katalog Steuerelement in Microsoft Paint für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f52e3-164">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot eines in-Ribbon Gallery-Steuer Elements im Microsoft Paint-Menüband.](images/controls/inribbongallery.png)

### <a name="combobox"></a><span data-ttu-id="f52e3-166">Kombinationsfeld</span><span class="sxs-lookup"><span data-stu-id="f52e3-166">ComboBox</span></span>

<span data-ttu-id="f52e3-167">Ein Kombinations [**Feld**](windowsribbon-element-combobox.md) ist ein einspaltige Listenfeld, das eine Auflistung von Elementen mit einem statischen Steuerelement oder einem Bearbeitungs Steuerelement und einem Dropdown Pfeil enthält.</span><span class="sxs-lookup"><span data-stu-id="f52e3-167">A [**ComboBox**](windowsribbon-element-combobox.md) is a single-column list box that contains a collection of items with either a static control or edit control and dropdown arrow.</span></span> <span data-ttu-id="f52e3-168">Der Listenfeld Bereich des Steuer Elements wird angezeigt, wenn der Benutzer auf den Dropdown Pfeil klickt.</span><span class="sxs-lookup"><span data-stu-id="f52e3-168">The list box portion of the control is displayed when the user clicks the drop-down arrow.</span></span>

<span data-ttu-id="f52e3-169">Der folgende Screenshot veranschaulicht ein Menüband-Kombinations [Feld](windowsribbon-controls-combobox.md) -Steuerelement von Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="f52e3-169">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![Screenshot eines ComboBox-Steuer Elements im Microsoft Paint-Menüband.](images/controls/combobox.png)

<span data-ttu-id="f52e3-171">Da es sich bei der [**ComboBox**](windowsribbon-element-combobox.md) ausschließlich um einen Element Katalog handelt, werden Befehls Elemente nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f52e3-171">Because the [**ComboBox**](windowsribbon-element-combobox.md) is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="f52e3-172">Es ist auch das einzige Katalog Steuerelement, das keinen Befehlsbereich unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f52e3-172">It is also the only gallery control that does not support a Command Space.</span></span> <span data-ttu-id="f52e3-173">(Ein Befehlsbereich ist eine Auflistung von Befehlen, die im Markup deklariert und am unteren Rand einer Element Galerie oder Befehls Galerie aufgelistet werden.)</span><span class="sxs-lookup"><span data-stu-id="f52e3-173">(A Command Space is a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery.)</span></span>

<span data-ttu-id="f52e3-174">Das folgende Codebeispiel zeigt das Markup, das zum Deklarieren eines Befehls Raums mit drei Schaltflächen in einem [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f52e3-174">The following code example shows the markup required to declare a three-button Command Space in a [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



<span data-ttu-id="f52e3-175">Der folgende Screenshot veranschaulicht den drei-Schaltflächen-Befehlsbereich des vorangehenden Code Beispiels.</span><span class="sxs-lookup"><span data-stu-id="f52e3-175">The following screen shot illustrates the three-button Command Space of the preceding code example.</span></span>

![Screenshot eines Befehls Raums mit drei Schaltflächen in einer dropdowngallery.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a><span data-ttu-id="f52e3-177">Vorgehensweise beim Implementieren eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="f52e3-177">How to Implement a Gallery</span></span>

<span data-ttu-id="f52e3-178">In diesem Abschnitt werden die Implementierungsdetails von Menü Band Katalogen erläutert und erläutert, wie Sie in eine Menü Bandanwendung integriert werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-178">This section discusses the implementation details of Ribbon galleries and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="the-basic-components"></a><span data-ttu-id="f52e3-179">Die grundlegenden Komponenten</span><span class="sxs-lookup"><span data-stu-id="f52e3-179">The Basic Components</span></span>

<span data-ttu-id="f52e3-180">In diesem Abschnitt werden die Eigenschaften und Methoden beschrieben, die das Backbone dynamischer Inhalte im Menüband Framework bilden und das Hinzufügen, löschen, aktualisieren und anderweitig bearbeiten des Inhalts und des visuellen Layouts von Menü Band Katalogen zur Laufzeit unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f52e3-180">This section describes the set of properties and methods that form the backbone of dynamic content in the Ribbon framework and support adding, deleting, updating, and otherwise manipulating the content and visual layout of Ribbon galleries at run time.</span></span>

### <a name="iuicollection"></a><span data-ttu-id="f52e3-181">Iuicollection</span><span class="sxs-lookup"><span data-stu-id="f52e3-181">IUICollection</span></span>

<span data-ttu-id="f52e3-182">Kataloge benötigen einen grundlegenden Satz von Methoden, um auf die einzelnen Elemente in ihren Sammlungen zuzugreifen und Sie zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f52e3-182">Galleries require a basic set of methods to access and manipulate the individual items in their collections.</span></span>

<span data-ttu-id="f52e3-183">Die [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) -Schnittstelle definiert diese Methoden, und das Framework ergänzt ihre Funktionalität durch zusätzliche Methoden, die in der [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Schnittstelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f52e3-183">The [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) interface defines these methods, and the framework supplements their functionality with additional methods that are defined in the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="f52e3-184">**Iuicollection** wird vom Framework für jede Katalog Deklaration im Menü Band Markup implementiert.</span><span class="sxs-lookup"><span data-stu-id="f52e3-184">**IUICollection** is implemented by the framework for each gallery declaration in the Ribbon markup.</span></span>

<span data-ttu-id="f52e3-185">Wenn zusätzliche Funktionen erforderlich sind, die nicht von der [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Schnittstelle bereitgestellt werden, kann ein benutzerdefiniertes Auflistungs Objekt, das von der Host Anwendung implementiert und von [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) abgeleitet wurde, für die frameworkauflistung ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-185">If additional functionality is required that is not provided by the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface, then a custom collection object that is implemented by the host application and derived from [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) can be substituted for the framework collection.</span></span>

### <a name="iuicollectionchangedevent"></a><span data-ttu-id="f52e3-186">Iuicollectionchangede Vent</span><span class="sxs-lookup"><span data-stu-id="f52e3-186">IUICollectionChangedEvent</span></span>

<span data-ttu-id="f52e3-187">Damit eine Anwendung auf Änderungen in einer Galerie Auflistung antwortet, muss Sie die [**iuicollectionchangedebug**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="f52e3-187">For an application to respond to changes in a gallery collection, it must implement the [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) interface.</span></span> <span data-ttu-id="f52e3-188">Anwendungen können Benachrichtigungen von einem [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt über den [**iuicollectionchangedevent:: OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) -Ereignislistener abonnieren.</span><span class="sxs-lookup"><span data-stu-id="f52e3-188">Applications can subscribe to notifications from an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [**IUICollectionChangedEvent::OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) event listener.</span></span>

<span data-ttu-id="f52e3-189">Wenn die Anwendung die vom Framework bereitgestellte Galerie Auflistung durch eine benutzerdefinierte Auflistung ersetzt, sollte die Anwendung die [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="f52e3-189">When the application replaces the gallery collection provided by the framework with a custom collection, the application should implement the [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface.</span></span> <span data-ttu-id="f52e3-190">Wenn [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) nicht implementiert ist, kann die Anwendung das Framework von Änderungen in der benutzerdefinierten Sammlung, die dynamische Aktualisierungen des Katalog-Steuer Elements erfordern, nicht benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="f52e3-190">If [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, then the application is unable to notify the framework of changes in the custom collection that require dynamic updates to the gallery control.</span></span>

<span data-ttu-id="f52e3-191">In Fällen, in denen [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) nicht implementiert ist, kann das Katalog-Steuerelement nur durch die Invalidierung durch [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) und [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)oder durch Aufrufen von [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-191">In those cases where [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, the gallery control can be updated only by invalidation through [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) and [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty), or by calling [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>

### <a name="iuisimplepropertyset"></a><span data-ttu-id="f52e3-192">Iuisimplepropertyset</span><span class="sxs-lookup"><span data-stu-id="f52e3-192">IUISimplePropertySet</span></span>

<span data-ttu-id="f52e3-193">Anwendungen müssen iuisimplepropertyset für jedes Element oder jeden Befehl in einer Galerie Auflistung implementieren.</span><span class="sxs-lookup"><span data-stu-id="f52e3-193">Applications must implement IUISimplePropertySet for each item or Command in a gallery collection.</span></span> <span data-ttu-id="f52e3-194">Die Eigenschaften, die mit [**iuisimplepropertyset:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) angefordert werden können, sind jedoch unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="f52e3-194">However, the properties that can be requested with [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) vary.</span></span>

<span data-ttu-id="f52e3-195">Elemente werden über den Benutzeroberflächen- [ \_ pkey \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) -Eigenschafts Schlüssel definiert und an einen Katalog gebunden, und es werden Eigenschaften mit einem [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="f52e3-195">Items are defined and bound to a gallery through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key and expose properties with an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="f52e3-196">Die gültigen Eigenschaften für Elemente in Element Galerien ([**UI \_ CommandType \_ Collection**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f52e3-196">The valid properties for items in item galleries ([**UI\_COMMANDTYPE\_COLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="f52e3-197">Einige Element Eigenschaften, z. b. die [UI- \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md), können im Markup definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-197">Some item properties, such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), can be defined in markup.</span></span> <span data-ttu-id="f52e3-198">Weitere Details finden Sie in der Referenz Dokumentation zu [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="f52e3-198">For more detail, see the [Property Keys](windowsribbon-reference-properties.md) reference documentation.</span></span>

 



<span data-ttu-id="f52e3-199">Control</span><span class="sxs-lookup"><span data-stu-id="f52e3-199">Control</span></span>

<span data-ttu-id="f52e3-200">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f52e3-200">Properties</span></span>

[<span data-ttu-id="f52e3-201">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="f52e3-201">**ComboBox**</span></span>](windowsribbon-element-combobox.md)

<span data-ttu-id="f52e3-202">[Benutzeroberfläche \_ Pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f52e3-202">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="f52e3-203">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="f52e3-203">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)

<span data-ttu-id="f52e3-204">[Benutzeroberfläche \_ Pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ itemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f52e3-204">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="f52e3-205">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="f52e3-205">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)

<span data-ttu-id="f52e3-206">[Benutzeroberfläche \_ Pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ itemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f52e3-206">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="f52e3-207">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="f52e3-207">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)

<span data-ttu-id="f52e3-208">[Benutzeroberfläche \_ Pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ itemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f52e3-208">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

<span data-ttu-id="f52e3-209">[Benutzeroberfläche \_ Pkey \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) ist eine Eigenschaft der Element Galerie.</span><span class="sxs-lookup"><span data-stu-id="f52e3-209">[UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) is a property of the item gallery.</span></span>



 

<span data-ttu-id="f52e3-210">Die gültigen Element Eigenschaften für Befehls Galerien ([**UI \_ CommandType \_ CommandCollection**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f52e3-210">The valid item properties for Command galleries ([**UI\_COMMANDTYPE\_COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>



| <span data-ttu-id="f52e3-211">Control</span><span class="sxs-lookup"><span data-stu-id="f52e3-211">Control</span></span>                                                                | <span data-ttu-id="f52e3-212">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f52e3-212">Properties</span></span>                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f52e3-213">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="f52e3-213">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       | <span data-ttu-id="f52e3-214">[Benutzeroberfläche \_ Pkey \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f52e3-214">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="f52e3-215">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="f52e3-215">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       | <span data-ttu-id="f52e3-216">[Benutzeroberfläche \_ Pkey \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f52e3-216">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="f52e3-217">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="f52e3-217">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) | <span data-ttu-id="f52e3-218">[Benutzeroberfläche \_ Pkey \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f52e3-218">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>  |



 

<span data-ttu-id="f52e3-219">Kategorien werden verwendet, um Elemente und Befehle in Galerien zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="f52e3-219">Categories are used to organize items and Commands in galleries.</span></span> <span data-ttu-id="f52e3-220">Kategorien werden mithilfe des Eigenschafts Schlüssels der UI- [ \_ pkey- \_ Kategorien](windowsribbon-reference-properties-uipkey-categories.md) definiert und an einen Katalog gebunden, und es werden Eigenschaften mit einem kategoriespezifischen [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="f52e3-220">Categories are defined and bound to a gallery through the [UI\_PKEY\_Categories](windowsribbon-reference-properties-uipkey-categories.md) property key and expose properties with a category-specific [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="f52e3-221">Kategorien haben keinen CommandType und unterstützen keine Benutzerinteraktion.</span><span class="sxs-lookup"><span data-stu-id="f52e3-221">Categories do not have a CommandType and do not support user interaction.</span></span> <span data-ttu-id="f52e3-222">Beispielsweise können Kategorien nicht zum SelectedItem in einem Element Katalog werden, und Sie sind nicht an einen Befehl in einer Befehls Galerie gebunden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-222">For example, categories cannot become the SelectedItem in an item gallery, and they are not bound to a Command in a Command gallery.</span></span> <span data-ttu-id="f52e3-223">Wie andere Katalog Element Eigenschaften können auch Kategorieeigenschaften wie " [UI \_ pkey \_](windowsribbon-reference-properties-uipkey-label.md) " und " [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) " durch Aufrufen von " [**iuisimplepropertyset:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-223">Like other gallery item properties, category properties such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) and [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) can be retrieved by calling [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f52e3-224">[**Iuisimplepropertyset:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) sollte den [**benutzeroberflächensammlungs- \_ \_ InvalidIndex**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) zurückgeben, wenn die [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) für ein Element angefordert wird, dem keine Kategorie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f52e3-224">[**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) should return [**UI\_COLLECTION\_INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) when [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) is requested for an item that does not have an associated category.</span></span>

 

### <a name="declare-the-controls-in-markup"></a><span data-ttu-id="f52e3-225">Deklarieren der Steuerelemente im Markup</span><span class="sxs-lookup"><span data-stu-id="f52e3-225">Declare the Controls in Markup</span></span>

<span data-ttu-id="f52e3-226">Galerien müssen wie alle Menü Band Steuerelemente im Markup deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-226">Galleries, like all Ribbon controls, must be declared in markup.</span></span> <span data-ttu-id="f52e3-227">Ein Katalog wird im Markup als Element Katalog oder Befehls Katalog identifiziert, und verschiedene Präsentations Details werden deklariert.</span><span class="sxs-lookup"><span data-stu-id="f52e3-227">A gallery is identified in markup as an item gallery or Command gallery, and various presentation details are declared.</span></span> <span data-ttu-id="f52e3-228">Im Gegensatz zu anderen Steuerelementen ist es für Kataloge erforderlich, dass nur der Basis Steuerelement-oder Sammlungs Container im Markup deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="f52e3-228">Unlike other controls, galleries require the base control only, or collection container, to be declared in markup.</span></span> <span data-ttu-id="f52e3-229">Die tatsächlichen Sammlungen werden zur Laufzeit aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f52e3-229">The actual collections are populated at run time.</span></span> <span data-ttu-id="f52e3-230">Wenn ein Katalog im Markup deklariert wird, wird mit dem *Type* -Attribut angegeben, ob es sich bei dem Katalog um eine Element Galerie einer Befehls Galerie handelt.</span><span class="sxs-lookup"><span data-stu-id="f52e3-230">When a gallery is declared in markup, the *Type* attribute is used to specify whether the gallery is an item gallery of a Command gallery.</span></span>

<span data-ttu-id="f52e3-231">Es gibt eine Reihe optionaler Layoutattribute, die für jedes der hier beschriebenen Steuerelemente verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f52e3-231">There are a number of optional layout attributes available for each of the controls discussed here.</span></span> <span data-ttu-id="f52e3-232">Diese Attribute stellen Entwicklereinstellungen für das Framework zur Verfügung, die sich direkt darauf auswirken, wie ein Steuerelement in einem Menüband aufgefüllt und angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f52e3-232">These attributes provide developer preferences for the framework to follow that directly affect how a control is populated and displayed in a ribbon.</span></span> <span data-ttu-id="f52e3-233">Die in Markup anwendbaren Einstellungen beziehen sich auf die Anzeige-und Layoutvorlagen und Verhaltensweisen, die unter [Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md)erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-233">The preferences applicable in markup are related to the display and layout templates and behaviors discussed in [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="f52e3-234">Wenn ein bestimmtes Steuerelement keine Layouteinstellungen direkt im Markup zulässt oder die Layouteinstellungen nicht angegeben sind, definiert das Framework Steuerelement spezifische Anzeige Konventionen basierend auf der Menge des verfügbaren Bildschirm Raums.</span><span class="sxs-lookup"><span data-stu-id="f52e3-234">If a particular control does not allow layout preferences directly in markup, or the layout preferences are not specified, then the framework defines control-specific display conventions based on the amount of screen space available.</span></span>

<span data-ttu-id="f52e3-235">In den folgenden Beispielen wird veranschaulicht, wie Sie einen Satz von Galerien in eine Multifunktionsleiste integrieren.</span><span class="sxs-lookup"><span data-stu-id="f52e3-235">The following examples demonstrate how to incorporate a set of galleries into a Ribbon.</span></span>

### <a name="command-declarations"></a><span data-ttu-id="f52e3-236">Befehls Deklarationen</span><span class="sxs-lookup"><span data-stu-id="f52e3-236">Command Declarations</span></span>

<span data-ttu-id="f52e3-237">Befehle sollten mit einem *CommandName* -Attribut deklariert werden, das zum Zuordnen eines Steuer Elements oder einer Gruppe von Steuerelementen mit dem Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f52e3-237">Commands should be declared with a *CommandName* attribute that is used to associate a control, or set of controls, with the Command.</span></span>

<span data-ttu-id="f52e3-238">Ein *CommandID* -Attribut, das zum Binden eines Befehls an einen Befehls Handler verwendet wird, wenn das Markup kompiliert wird, kann auch hier angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-238">A *CommandId* attribute used to bind a Command to a Command handler when the markup is compiled can also be specified here.</span></span> <span data-ttu-id="f52e3-239">Wenn keine ID angegeben ist, wird eine von dem Framework generiert.</span><span class="sxs-lookup"><span data-stu-id="f52e3-239">If no ID is provided, then one is generated by the framework.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a><span data-ttu-id="f52e3-240">Steuerelement Deklarationen</span><span class="sxs-lookup"><span data-stu-id="f52e3-240">Control Declarations</span></span>

<span data-ttu-id="f52e3-241">Dieser Abschnitt enthält Beispiele, die das grundlegende Steuerelement Markup veranschaulichen, das für die verschiedenen Katalog Typen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f52e3-241">This section contains examples that demonstrate the basic control markup required for the various gallery types.</span></span> <span data-ttu-id="f52e3-242">Sie zeigen, wie die Katalog Steuerelemente deklariert und mit einem Befehl über das *CommandName* -Attribut verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-242">They show how to declare the gallery controls and associate them with a Command through the *CommandName* attribute.</span></span>

<span data-ttu-id="f52e3-243">Das folgende Beispiel zeigt eine Steuerelement Deklaration für [**dropdowngallery**](windowsribbon-element-dropdowngallery.md) , in der das *Type* -Attribut verwendet wird, um anzugeben, dass es sich um eine Befehls Galerie handelt.</span><span class="sxs-lookup"><span data-stu-id="f52e3-243">The following example shows a control declaration for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) where the *Type* attribute is used to specify that this is a Command gallery.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



<span data-ttu-id="f52e3-244">Das folgende Beispiel zeigt eine Steuerelement Deklaration für den [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="f52e3-244">The following example shows a control declaration for the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



<span data-ttu-id="f52e3-245">Das folgende Beispiel zeigt eine Steuerelement Deklaration für den [**inribbongallery**](windowsribbon-element-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="f52e3-245">The following example shows a control declaration for the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).</span></span>

> [!Note]  
> <span data-ttu-id="f52e3-246">Da der [**inribbongallery**](windowsribbon-element-inribbongallery.md) so konzipiert ist, dass er eine Teilmenge der Element Auflistung im Menüband anzeigt, ohne ein Dropdown Menü zu aktivieren, bietet er eine Reihe optionaler Attribute, die seine Größe und das Element Layout bei der Menü Band Initialisierung steuern.</span><span class="sxs-lookup"><span data-stu-id="f52e3-246">Because the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is designed to display a subset of its item collection in the Ribbon without activating a drop-down menu, it provides a number of optional attributes that govern its size and item layout on Ribbon initialization.</span></span> <span data-ttu-id="f52e3-247">Diese Attribute sind für den **inribbongallery** eindeutig und nicht in den anderen dynamischen Steuerelementen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f52e3-247">These attributes are unique to the **InRibbonGallery** and are not available from the other dynamic controls.</span></span>

 


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



<span data-ttu-id="f52e3-248">Das folgende Beispiel zeigt eine Steuerelement Deklaration für das [**ComboBox**](windowsribbon-element-combobox.md)-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="f52e3-248">The following example shows a control declaration for the [**ComboBox**](windowsribbon-element-combobox.md).</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a><span data-ttu-id="f52e3-249">Erstellen eines Befehls Handlers</span><span class="sxs-lookup"><span data-stu-id="f52e3-249">Create a Command Handler</span></span>

<span data-ttu-id="f52e3-250">Für jeden Befehl erfordert das Menüband-Framework einen entsprechenden Befehls Handler in der Host Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f52e3-250">For each Command, the Ribbon framework requires a corresponding Command handler in the host application.</span></span> <span data-ttu-id="f52e3-251">Befehls Handler werden von der Menüband-Host Anwendung implementiert und werden von der [**iuicommandhandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) -Schnittstelle abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f52e3-251">Command handlers are implemented by the Ribbon host application and are derived from the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span>

> [!Note]  
> <span data-ttu-id="f52e3-252">Mehrere Befehle können an einen einzelnen Befehls Handler gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-252">Multiple Commands can be bound to a single Command handler.</span></span>

 

<span data-ttu-id="f52e3-253">Ein Befehls Handler dient zwei Zwecken:</span><span class="sxs-lookup"><span data-stu-id="f52e3-253">A Command handler serves two purposes:</span></span>

-   <span data-ttu-id="f52e3-254">[**Iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) antwortet auf Aktualisierungs Anforderungen für Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f52e3-254">[**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) responds to property update requests.</span></span> <span data-ttu-id="f52e3-255">Die Werte der Befehls Eigenschaften, z. b. [ \_ \_ aktivierte UI pkey](windowsribbon-reference-properties-uipkey-enabled.md) -oder [UI \_ pkey \_](windowsribbon-reference-properties-uipkey-label.md)-Bezeichnungen, werden durch Aufrufe von [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) oder [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f52e3-255">The values of Command properties, such as [UI\_PKEY\_Enabled](windowsribbon-reference-properties-uipkey-enabled.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), are set through calls to [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) or [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span>
-   <span data-ttu-id="f52e3-256">[**Iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) antwortet auf Execute-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="f52e3-256">[**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) responds to execute events.</span></span> <span data-ttu-id="f52e3-257">Diese Methode unterstützt die folgenden drei Ausführungs Zustände, die durch den [**UI \_ executionverb**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) -Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-257">This method supports the following three execution states that are specified by the [**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) parameter.</span></span>
    -   <span data-ttu-id="f52e3-258">Der Ausführungs Status führt alle Befehle aus, an die der Handler gebunden ist, oder führt Sie aus.</span><span class="sxs-lookup"><span data-stu-id="f52e3-258">The Execute state executes, or commits to, any commands to which the handler is bound.</span></span>
    -   <span data-ttu-id="f52e3-259">Der Vorschau Zustand zeigt eine Vorschau der Befehle an, an die der Handler gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="f52e3-259">The Preview state previews any commands to which the handler is bound.</span></span> <span data-ttu-id="f52e3-260">Dadurch werden die Befehle ausgeführt, ohne dass ein Commit für das Ergebnis ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f52e3-260">This essentially executes the commands without committing to the result.</span></span>
    -   <span data-ttu-id="f52e3-261">Der cancelpreview-Status bricht alle in der Vorschau angezeigten Befehle ab.</span><span class="sxs-lookup"><span data-stu-id="f52e3-261">The CancelPreview state cancels any previewed Commands.</span></span> <span data-ttu-id="f52e3-262">Dies ist erforderlich, um die Traversierung über ein Menü oder eine Liste und eine sequenzielle Vorschau zu unterstützen und die Ergebnisse nach Bedarf rückgängig zu machen</span><span class="sxs-lookup"><span data-stu-id="f52e3-262">This is required to support traversal through a menu or list and sequentially preview and undo the results as required.</span></span>

<span data-ttu-id="f52e3-263">Im folgenden Beispiel wird ein Katalog Befehls Handler veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f52e3-263">The following example demonstrates a gallery command handler.</span></span>


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a><span data-ttu-id="f52e3-264">Binden des Befehls Handlers</span><span class="sxs-lookup"><span data-stu-id="f52e3-264">Bind the Command Handler</span></span>

<span data-ttu-id="f52e3-265">Nachdem Sie einen Befehls Handler definiert haben, muss der Befehl an den Handler gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-265">After you define a Command handler, the Command must be bound to the handler.</span></span>

<span data-ttu-id="f52e3-266">Im folgenden Beispiel wird veranschaulicht, wie ein Galerie Befehl an einen bestimmten Befehls Handler gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="f52e3-266">The following example demonstrates how to bind a gallery Command to a specific Command handler.</span></span> <span data-ttu-id="f52e3-267">In diesem Fall werden die [**ComboBox**](windowsribbon-element-combobox.md) -Steuerelemente und die Gallery-Steuerelemente an die entsprechenden Befehls Handler gebunden.</span><span class="sxs-lookup"><span data-stu-id="f52e3-267">In this case, both the [**ComboBox**](windowsribbon-element-combobox.md) and gallery controls are bound to their respective Command handlers.</span></span>


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a><span data-ttu-id="f52e3-268">Initialisieren einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="f52e3-268">Initialize a Collection</span></span>

<span data-ttu-id="f52e3-269">Im folgenden Beispiel wird eine benutzerdefinierte Implementierung von [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) für Element-und Befehls Galerien veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f52e3-269">The following example demonstrates a custom implementation of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) for both item and Command galleries.</span></span>

<span data-ttu-id="f52e3-270">Die citemproperties-Klasse in diesem Beispiel wird von [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f52e3-270">The CItemProperties class in this example is derived from [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset).</span></span> <span data-ttu-id="f52e3-271">Zusätzlich zur erforderlichen [**iuisimplepropertyset:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)-Methode implementiert die citemproperties-Klasse einen Satz von Hilfsfunktionen für die Initialisierung und Index Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="f52e3-271">In addition to the required method [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), the CItemProperties class implements a set of helper functions for initialization and index tracking.</span></span>


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a><span data-ttu-id="f52e3-272">Behandeln von Sammlungs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f52e3-272">Handle Collection Events</span></span>

<span data-ttu-id="f52e3-273">Im folgenden Beispiel wird eine iuicollectionchangedebug-Implementierung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f52e3-273">The following example demonstrates an IUICollectionChangedEvent implementation.</span></span>


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="f52e3-274">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f52e3-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f52e3-275">Sammlungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f52e3-275">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="f52e3-276">Erstellen einer Menü Bandanwendung</span><span class="sxs-lookup"><span data-stu-id="f52e3-276">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="f52e3-277">Grundlegendes zu Befehlen und Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="f52e3-277">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> <dt>

[<span data-ttu-id="f52e3-278">Multifunktionsleisten-Benutzeroberflächen Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f52e3-278">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="f52e3-279">Menüband-Entwurfsprozess</span><span class="sxs-lookup"><span data-stu-id="f52e3-279">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[<span data-ttu-id="f52e3-280">Galerie Beispiel</span><span class="sxs-lookup"><span data-stu-id="f52e3-280">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 