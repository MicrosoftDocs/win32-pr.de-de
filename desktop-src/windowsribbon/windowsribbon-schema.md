---
title: Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup
description: Das Windows-Menü Band Framework verwendet eine Markup Sprache, die auf Extensible Application Markup Language (XAML) basiert, um die Darstellung einer Menü Bandanwendung deklarativ zu implementieren.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Windows-Menüband, Markup Struktur
- Menüband, Markup Struktur
- Windows-Menüband, Trennen der Präsentation von der Befehls Logik
- Multifunktionsleiste, Trennen der Präsentation von der Befehls Logik
- Windows-Menüband, Komponenten
- Multifunktionsleiste, Komponenten
- Befehlssystem für Windows-Menüband
- Steuerelemente für Windows-Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c5c193332ce217709c825a58f0ae546c03c9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390739"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a><span data-ttu-id="f9570-111">Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup</span><span class="sxs-lookup"><span data-stu-id="f9570-111">Declaring Commands and Controls with Ribbon Markup</span></span>

<span data-ttu-id="f9570-112">Das Windows-Menü Band Framework verwendet eine Markup Sprache, die auf Extensible Application Markup Language (XAML) basiert, um die Darstellung einer Menü Bandanwendung deklarativ zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="f9570-112">The Windows Ribbon framework uses a markup language based on Extensible Application Markup Language (XAML) to declaratively implement the appearance of a Ribbon application.</span></span>

-   [<span data-ttu-id="f9570-113">Trennen der Präsentation von der Befehls Logik</span><span class="sxs-lookup"><span data-stu-id="f9570-113">Separating Presentation from Command Logic</span></span>](#separating-presentation-from-command-logic)
-   [<span data-ttu-id="f9570-114">Markup Struktur</span><span class="sxs-lookup"><span data-stu-id="f9570-114">Markup Structure</span></span>](#markup-structure)
-   [<span data-ttu-id="f9570-115">Menü Band Komponenten</span><span class="sxs-lookup"><span data-stu-id="f9570-115">Ribbon Components</span></span>](#ribbon-components)
-   [<span data-ttu-id="f9570-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9570-116">Related topics</span></span>](#related-topics)

## <a name="separating-presentation-from-command-logic"></a><span data-ttu-id="f9570-117">Trennen der Präsentation von der Befehls Logik</span><span class="sxs-lookup"><span data-stu-id="f9570-117">Separating Presentation from Command Logic</span></span>

<span data-ttu-id="f9570-118">Die Trennung von Präsentations-und visuellen Attributen von der Befehls Logik im Menüband-Framework erfolgt über zwei unterschiedliche, aber abhängige Entwicklungsplattformen.</span><span class="sxs-lookup"><span data-stu-id="f9570-118">The separation of presentation and visual attributes from command logic in the Ribbon framework is accomplished through two distinct, but dependent, development platforms.</span></span> <span data-ttu-id="f9570-119">Steuerelement Layouts, Skalierungs Verhalten, Befehls Deklarationen und Ressourcen Spezifikationen sind die Entwurfszeit Domäne einer deklarativen Markup Syntax, die auf der [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) -Spezifikation basiert.</span><span class="sxs-lookup"><span data-stu-id="f9570-119">Control layouts, scaling behaviors, Command declarations, and resource specifications are the design time domain of a declarative markup syntax based on the [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) specification.</span></span> <span data-ttu-id="f9570-120">Funktionen auf niedriger Ebene, Anwendungs Hooks und Befehls Handler werden in Component Object Model (com)-basierten Schnittstellen Implementierungen definiert.</span><span class="sxs-lookup"><span data-stu-id="f9570-120">Low level functionality, application hooks, and Command handlers are defined in Component Object Model (COM)-based interface implementations.</span></span>

<span data-ttu-id="f9570-121">Diese Trennung von Präsentation und Logik bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="f9570-121">This separation of presentation and logic provides the following benefits:</span></span>

-   <span data-ttu-id="f9570-122">Ein effizienterer Anwendungs Entwicklungs Cycle, mit dem Benutzeroberflächen Entwickler und Designer die GUI der Menüband-Anwendung unabhängig von der Kern Anwendungs Funktionalität implementieren können.</span><span class="sxs-lookup"><span data-stu-id="f9570-122">A more efficient application development cycle which allows UI developers and designers to implement the GUI of the Ribbon application independently from the core application functionality.</span></span> <span data-ttu-id="f9570-123">Diese Kernfunktionen können dedizierten Softwareentwicklern überlassen werden.</span><span class="sxs-lookup"><span data-stu-id="f9570-123">This core functionality can be left to dedicated software developers.</span></span>
-   <span data-ttu-id="f9570-124">Kostengünstigere Wartung, da Änderungen an der GUI ohne Änderungen an der Kernfunktionalität (und umgekehrt) möglich sind.</span><span class="sxs-lookup"><span data-stu-id="f9570-124">Less costly maintenance because changes to the GUI are possible without changes to core functionality (and vice versa).</span></span>
-   <span data-ttu-id="f9570-125">Einfache Angabe von Zeichen folgen-und Bild Ressourcen durch Markup.</span><span class="sxs-lookup"><span data-stu-id="f9570-125">Simple specification of string and image resources through markup.</span></span>
-   <span data-ttu-id="f9570-126">Einfache Prototyperstellung.</span><span class="sxs-lookup"><span data-stu-id="f9570-126">Ease of prototyping.</span></span>

## <a name="markup-structure"></a><span data-ttu-id="f9570-127">Markup Struktur</span><span class="sxs-lookup"><span data-stu-id="f9570-127">Markup Structure</span></span>

<span data-ttu-id="f9570-128">Innerhalb der Struktur von Multifunktionsleisten-Frameworks sind zwei unterschiedliche Verzweigungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f9570-128">Two distinct branches exist within the structure of Ribbon framework markup.</span></span>

<span data-ttu-id="f9570-129">Der erste Branch enthält ein Manifest von Befehls-und Ressourcen Deklarationen (Zeichen folgen und Bilder).</span><span class="sxs-lookup"><span data-stu-id="f9570-129">The first branch contains a manifest of Command and resource declarations (strings and images).</span></span> <span data-ttu-id="f9570-130">Jeder Befehls Eintrag wird vom Framework verwendet, um ein Menüband-Steuerelement über eine Befehls-ID an einen Befehls Handler zu binden, der im Anwendungscode definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9570-130">Each Command entry is used by the framework to bind a Ribbon control, through a Command ID, to a Command handler defined in the application code.</span></span>

<span data-ttu-id="f9570-131">Die zweite Verzweigung enthält die tatsächlichen Steuerelement Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="f9570-131">The second branch contains the actual control declarations.</span></span> <span data-ttu-id="f9570-132">Jedes Steuerelement ist einem Befehl über ein *CommandName* -Attribut zugeordnet, das einem *namens* Attribut zugeordnet ist, das in jeder Befehls Deklaration angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f9570-132">Each control is associated with a Command through a *CommandName* attribute that maps to a *Name* attribute specified in each Command declaration.</span></span>

## <a name="ribbon-components"></a><span data-ttu-id="f9570-133">Menü Band Komponenten</span><span class="sxs-lookup"><span data-stu-id="f9570-133">Ribbon Components</span></span>

<span data-ttu-id="f9570-134">Die Benutzeroberfläche des Multifunktionsleisten-Frameworks wird durch [Ansichten](windowsribbon-reference-elements-view.md)verfügbar gemacht</span><span class="sxs-lookup"><span data-stu-id="f9570-134">Ribbon framework UI functionality is exposed through [Views](windowsribbon-reference-elements-view.md).</span></span> <span data-ttu-id="f9570-135">Eine Sicht ist im Wesentlichen ein Container, z. b. das [**Menüband**](windowsribbon-element-ribbon.md) und [**contextpopup**](windowsribbon-element-contextpopup.md), das verwendet wird, um frameworksteuerelemente und die Befehle darzustellen, an die Sie gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="f9570-135">A View is essentially a container, such as the [**Ribbon**](windowsribbon-element-ribbon.md) and [**ContextPopup**](windowsribbon-element-contextpopup.md), that is used to present framework controls and the Commands they are bound to.</span></span>

<span data-ttu-id="f9570-136">Die Ansicht " [**Menüband**](windowsribbon-element-ribbon.md) " besteht aus mehreren Komponenten, die ein [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)enthalten, der [Symbolleiste für den schnell Zugriff (QAT)](windowsribbon-controls-quickaccesstoolbar.md) zum Anzeigen häufig verwendeter Befehle von der Multifunktionsleisten-Benutzeroberfläche, von Kern-und Kontext [Registerkarten](windowsribbon-controls-tab.md) , die [Gruppen](windowsribbon-controls-group.md) von Steuerelementen enthalten, und vom umfangreichen Kontextmenü System von [**contextpopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="f9570-136">The [**Ribbon**](windowsribbon-element-ribbon.md) View is composed of several components that include an [Application Menu](windowsribbon-controls-applicationmenu.md), the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md) for displaying commonly used Commands from the ribbon UI, core and contextual [tabs](windowsribbon-controls-tab.md) that contain [groups](windowsribbon-controls-group.md) of controls, and the rich context menu system of the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="f9570-137">Alle Multifunktionsleistenkomponenten werden in einer eigenständigen Markup Datei deklariert:</span><span class="sxs-lookup"><span data-stu-id="f9570-137">All Ribbon components are declared in a standalone markup file that:</span></span>

-   <span data-ttu-id="f9570-138">Gibt die grundlegenden Eigenschaften für jedes Element an.</span><span class="sxs-lookup"><span data-stu-id="f9570-138">Specifies the basic properties for each element.</span></span>
-   <span data-ttu-id="f9570-139">Zeigt hierarchische Beziehungen eindeutig an.</span><span class="sxs-lookup"><span data-stu-id="f9570-139">Shows hierarchical relationships clearly.</span></span>
-   <span data-ttu-id="f9570-140">Liefert Layouteinstellungen und Skalierungs Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f9570-140">Supplies layout preferences and scaling hints.</span></span> <span data-ttu-id="f9570-141">Weitere Informationen zu Menüband-frameworklayoutvorlagen finden Sie unter [Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="f9570-141">For more information on Ribbon framework layout templates, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>
-   <span data-ttu-id="f9570-142">Bietet eine Möglichkeit, Ressourcen wie Bilder und Bezeichnungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f9570-142">Provides a way to define resources such as images and labels.</span></span> <span data-ttu-id="f9570-143">Weitere Informationen zu Bild Ressourcen finden Sie unter [Angeben von Menüband-Bild Ressourcen](windowsribbon-imageformats.md).</span><span class="sxs-lookup"><span data-stu-id="f9570-143">For more information on image resources, see [Specifying Ribbon Image Resources](windowsribbon-imageformats.md).</span></span>

<span data-ttu-id="f9570-144">Die beiden folgenden Beispiele für Menü Band Markierungen veranschaulichen, wie ein Satz von Menü Elementen der Menü Bandanwendung jeweils mit einem Befehlsnamen und einer ID verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="f9570-144">The following two Ribbon markup examples demonstrate how a set of Ribbon Application Menu items are each associated with a Command name and ID.</span></span>

1.  <span data-ttu-id="f9570-145">In diesem Abschnitt werden die für ein Anwendungsmenü erforderlichen Befehls Deklarationen mit grundlegenden Befehlen wie "New", "Open" und "Save" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f9570-145">This section shows the Command declarations required for an Application Menu with basic commands such as New, Open, and Save.</span></span>
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  <span data-ttu-id="f9570-146">Dieser Abschnitt zeigt die zugeordneten Steuerelement Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="f9570-146">This section shows the associated Control declarations.</span></span>
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

<span data-ttu-id="f9570-147">Wenn das Markup mit dem UI-Befehls Compiler (UICC) kompiliert wird, werden die Befehlsnamen und IDs in einer von der Menüband-Host Anwendung verwendeten Header Datei abgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9570-147">When the markup is compiled with the UI Command Compiler (UICC) tool, the Command names and IDs are placed into a header file used by the Ribbon host application.</span></span>

<span data-ttu-id="f9570-148">Im folgenden finden Sie ein Beispiel für eine Header Datei, die von UICC generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f9570-148">The following is an example of a header file generated by UICC.</span></span>


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a><span data-ttu-id="f9570-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9570-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9570-150">Extensible Application Markup Language (XAML)</span><span class="sxs-lookup"><span data-stu-id="f9570-150">Extensible Application Markup Language (XAML)</span></span>](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[<span data-ttu-id="f9570-151">Kompilieren von Menü Band Markup</span><span class="sxs-lookup"><span data-stu-id="f9570-151">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)
</dt> </dl>

 

 