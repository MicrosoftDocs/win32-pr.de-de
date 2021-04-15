---
title: Grundlegendes zu Befehlen und Steuerelementen
description: Die Trennung der Logik von der Präsentation ist die Entwurfs Philosophie, die das Befehls Präsentationssystem von Windows Ribbon Framework \ 8212 inspiriert; ein System, das auf einem Entwurfsmuster basiert, in dem Funktionalität und Verhalten unabhängig von den Steuerelementen implementiert werden, die diese Funktionalität verfügbar machen.
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Fenster Multifunktionsleiste, Befehle (Übersicht)
- Menüband, Befehle (Übersicht)
- Fenster Multifunktionsleiste, Übersicht über Steuerelemente
- Menüband, Übersicht über Steuerelemente
- Befehlssystem für Windows-Menüband
- Steuerelemente für Windows-Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104556722"
---
# <a name="understanding-commands-and-controls"></a><span data-ttu-id="b5cd9-109">Grundlegendes zu Befehlen und Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="b5cd9-109">Understanding Commands and Controls</span></span>

<span data-ttu-id="b5cd9-110">Die Trennung der Logik von der Präsentation ist die Entwurfs Philosophie, die das Befehls Präsentationssystem des Windows-Menüband-Frameworks – ein System, das auf einem Entwurfsmuster basiert, bei dem Funktionalität und Verhalten unabhängig von den Steuerelementen implementiert werden, die diese Funktionalität verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-110">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Windows Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

-   [<span data-ttu-id="b5cd9-111">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="b5cd9-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="b5cd9-112">Das Windows-Menüband-Befehls System</span><span class="sxs-lookup"><span data-stu-id="b5cd9-112">The Windows Ribbon Command System</span></span>](#the-windows-ribbon-command-system)
    -   [<span data-ttu-id="b5cd9-113">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b5cd9-113">Controls</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="b5cd9-114">Befehle</span><span class="sxs-lookup"><span data-stu-id="b5cd9-114">Commands</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="b5cd9-115">Die Befehls Funktion in Aktion</span><span class="sxs-lookup"><span data-stu-id="b5cd9-115">The Command Experience In Action</span></span>](#the-command-experience-in-action)
-   [<span data-ttu-id="b5cd9-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5cd9-116">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="b5cd9-117">Einführung</span><span class="sxs-lookup"><span data-stu-id="b5cd9-117">Introduction</span></span>

<span data-ttu-id="b5cd9-118">In diesem Artikel wird das Design des befehlssystems des Menüband-Frameworks erläutert.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-118">This article discusses the design of the Ribbon framework command system.</span></span> <span data-ttu-id="b5cd9-119">Es beschreibt die Konzepte der Befehle und Steuerelemente und erläutert, wie diese zusammenarbeiten, um eine umfangreiche Befehls Oberfläche mit einer Reihe neuer Benutzeroberflächen Funktionen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-119">It describes the concepts of Commands and controls and explores how they work together to provide a rich command experience with a host of new UI capabilities.</span></span>

## <a name="the-windows-ribbon-command-system"></a><span data-ttu-id="b5cd9-120">Das Windows-Menüband-Befehls System</span><span class="sxs-lookup"><span data-stu-id="b5cd9-120">The Windows Ribbon Command System</span></span>

<span data-ttu-id="b5cd9-121">Im Menüband-Framework sind Befehle und Steuerelemente unabhängige Entitäten.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-121">In the Ribbon framework, Commands and controls are independent entities.</span></span> <span data-ttu-id="b5cd9-122">Ein Befehl ist eine abstrakte Struktur ohne Präsentations Einschränkungen, die eine bestimmte Aufgabe oder Funktionsklasse darstellt.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-122">A Command is an abstract structure, without presentation constraints, that represents a specific task or class of functionality.</span></span> <span data-ttu-id="b5cd9-123">Ein Steuerelement hingegen ist ein konkretes Objekt, das Befehlsfunktionen über die Multifunktionsleisten-Benutzeroberfläche verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-123">A control, on the other hand, is a concrete object that exposes Command functionality through the Ribbon UI.</span></span>

<span data-ttu-id="b5cd9-124">Diese Unterscheidung bietet die Möglichkeit, Befehle zu definieren, für die keine Benutzeroberflächen Details verfügbar sind und die für eine Aktion ausgeführt werden können, ohne dass Sie die Art und Weise verwalten müssen, wie die Aktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-124">This distinction provides the ability to define Commands that are free of UI details and able to execute on the intent of an action without the need to manage how the action was invoked.</span></span>

### <a name="controls"></a><span data-ttu-id="b5cd9-125">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b5cd9-125">Controls</span></span>

<span data-ttu-id="b5cd9-126">Steuerelemente sind die für die Befehls Darstellung erforderlichen UI-Objekte.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-126">Controls are the UI objects required for Command presentation.</span></span> <span data-ttu-id="b5cd9-127">Sie werden zur Laufzeit durch das Framework basierend auf der Benutzerinteraktion und einem Satz inhärenter Eigenschaften und Verhalten gerendert und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-127">They are rendered and managed at run time by the framework based on user interaction and a set of inherent properties and behaviors.</span></span>

<span data-ttu-id="b5cd9-128">Als Adaptive Layout bezeichnet die Framework-verwaltete Flexibilität der Benutzeroberfläche eine der großartigen Stärken der Multifunktionsleiste.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-128">Known as adaptive layout, the framework-managed flexibility of the UI is one of the great strengths of the Ribbon.</span></span> <span data-ttu-id="b5cd9-129">Menüband-Steuerelemente können sich automatisch durch Framework-abhängige oder Entwickler definierte Layoutvorlagen neu konfigurieren, die auf verschiedene Lauf Zeitanforderungen reagieren können, ohne eine einzige Zeile von Präsentationscode schreiben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-129">Ribbon controls can automatically reconfigure themselves through framework-dependent or developer-defined layout templates that are able to respond to various run time requirements, all without writing a single line of presentation code.</span></span> <span data-ttu-id="b5cd9-130">Weitere Informationen finden Sie unter [Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="b5cd9-130">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="b5cd9-131">Neben den Vorteilen des adaptiven Layouts bieten mehrere komplexe Menüband-Steuerelemente eigenständige Lösungen für bestimmte Bereiche von Benutzeroberflächen Problemen.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-131">Besides the benefits of adaptive layout, a number of complex Ribbon controls provide self-contained solutions for specific UI problem spaces.</span></span> <span data-ttu-id="b5cd9-132">Durch die Bereitstellung eines ausgereiften Interaktions Modells bieten multifunktionsleistensteuerelemente, wie z. b. FontControl oder ColorPicker, die Möglichkeit, Daten in abstrakter Form durch Eigenschafts Behälter tatsächlicher Schriftart-oder Farb Attribute und nicht durch verschiedene untergeordnete Steuerelemente, Enumerationen und Indexwerte von standardmäßigen Windows-Steuerelementen zu manipulieren.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-132">By offering a sophisticated interaction model, Ribbon controls, such as the FontControl or ColorPicker, provide the ability to manipulate data in more abstract terms through property bags of actual font or color attributes rather than through various sub-controls, enumerations, and index values of standard Windows controls.</span></span>

### <a name="commands"></a><span data-ttu-id="b5cd9-133">Befehle</span><span class="sxs-lookup"><span data-stu-id="b5cd9-133">Commands</span></span>

<span data-ttu-id="b5cd9-134">Wenn Sie locker an die Menüband-Steuerelemente gekoppelt sind, die ihre Funktionalität verfügbar machen, sind Befehls Implementierungen die Domäne der Host Anwendung und weisen die Form von Ereignislistenern, Befehls Handlern und verschiedenen Befehls Eigenschaften auf.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-134">Loosely coupled to the Ribbon controls that expose their functionality, Command implementations are the domain of the host application and take the form of event listeners, Command handlers, and various Command properties.</span></span>

<span data-ttu-id="b5cd9-135">Befehle werden im Menüband-Markup mit einer eindeutigen ID deklariert, oder bei der Kompilierung wurde eine vom Markup Compiler generierte ID zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-135">Commands are declared in Ribbon markup with a unique ID, or assigned a markup compiler-generated ID at compilation.</span></span> <span data-ttu-id="b5cd9-136">Befehle sind mit Steuerelementen über einen Befehlsnamen verknüpft, aber im Gegensatz zu-Steuerelementen wird Ihre tatsächliche Funktionalität in Code definiert, in dem Sie über die Befehls-ID an bestimmte Befehls Handler gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-136">Commands are associated with controls through a Command name but, unlike controls, their actual functionality is defined in code where they are bound to specific Command handlers through the Command ID.</span></span>

> [!Note]  
> <span data-ttu-id="b5cd9-137">Bei der Kompilierung wird diese ID in einer ID-Definitions Header Datei gespeichert, die Befehle für die entsprechenden Befehls Handler in der Menüband-Host Anwendung verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-137">At compilation, this ID is stored in an ID definition header file that exposes Commands to their corresponding Command handlers in the Ribbon host application.</span></span>

 

<span data-ttu-id="b5cd9-138">Jeder Befehl verfügt über einen zugrunde liegenden Befehlstyp, der in der [**UI \_ CommandType**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) -Enumeration aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-138">Each Command has an underlying Command type itemized in the [**UI\_COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) enumeration.</span></span>

### <a name="the-command-experience-in-action"></a><span data-ttu-id="b5cd9-139">Die Befehls Funktion in Aktion</span><span class="sxs-lookup"><span data-stu-id="b5cd9-139">The Command Experience In Action</span></span>

<span data-ttu-id="b5cd9-140">Die Funktionen dieses Befehls Modells werden von der Symbolleiste für den schnell Zugriff auf das Menüband (QAT) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-140">The capabilities of this command model are demonstrated by the Ribbon Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="b5cd9-141">QAT bietet Endbenutzern die Möglichkeit, auf einfache Weise ihre eigenen Verknüpfungen für praktisch alle Steuerelemente in der Menüband-Benutzeroberfläche zu definieren.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-141">The QAT provides end users with a way to easily define their own shortcuts for virtually any control in the Ribbon UI.</span></span> <span data-ttu-id="b5cd9-142">Der QAT wird zur Laufzeit dynamisch eine Verknüpfung hinzugefügt, wenn der Benutzer mit der rechten Maustaste auf ein Menüband-Steuerelement klickt und aus dem Kontextmenü die **Symbolleiste für den schnell Zugriff hinzufügen** auswählt.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-142">A shortcut is added dynamically to the QAT at run time when the user right-clicks a Ribbon control and selects **Add to Quick Access Toolbar** from the context menu.</span></span>

<span data-ttu-id="b5cd9-143">Das folgende Bild zeigt die Befehle **Einfügen** und **Einfügen aus** , dargestellt durch ein [**SplitButton**](windowsribbon-element-splitbutton.md) -Steuerelement im Menüband von Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-143">The following picture shows the **Paste** and **Paste from** Commands, represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon of Windows 7 Paint.</span></span>

![Bild der "SplitButton einfügen" im Microsoft Paint-Menüband.](images/overviews/paint-paste-splitbutton-ribbon.png)

<span data-ttu-id="b5cd9-145">Das folgende Bild zeigt die gleichen **Einfüge** -und **Einfüge Befehle von** Befehlen, die noch durch ein [**SplitButton**](windowsribbon-element-splitbutton.md) -Steuerelement dargestellt werden, im Menüband-QAT von Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-145">The following picture shows the same **Paste** and **Paste from** Commands, still represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon QAT of Windows 7 Paint.</span></span>

![Bild der "SplitButton einfügen" in Microsoft Paint QAT.](images/overviews/paint-paste-splitbutton-qat.png)

<span data-ttu-id="b5cd9-147">Wenn ein Steuerelement vom QAT gehostet wird, behält die neue Instanz des Steuer Elements die gesamte Funktionalität des ursprünglichen Steuer Elements bei, ohne dass zusätzliche Ereignislistener und Befehls Handler diese unterstützen müssen.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-147">When a control is hosted by the QAT, the new instance of the control maintains all the functionality of the original control without the need for additional event listeners and command handlers to support it.</span></span> <span data-ttu-id="b5cd9-148">Beide Steuerelemente werden über einen freigegebenen Befehls Bezeichner an denselben Menü Band Befehls Handler gebunden.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-148">Both controls are bound to the same Ribbon Command handler through a shared Command identifier.</span></span> <span data-ttu-id="b5cd9-149">Auf diese Weise behandelt das Framework beide Steuerelemente als eins, unabhängig davon, welches aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-149">In this way, the framework treats both controls as one, no matter which is invoked.</span></span>

> [!Note]  
> <span data-ttu-id="b5cd9-150">Die gleichen Vorteile werden erkannt, wenn Befehle zur Entwurfszeit in ein [**contextpopup-Objekt**](windowsribbon-element-contextpopup.md) integriert werden.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-150">The same benefits are realized when Commands are incorporated into a [**ContextPopup**](windowsribbon-element-contextpopup.md) at design time.</span></span> <span data-ttu-id="b5cd9-151">In diesem Fall können die Befehls Handler für das Einfügen verwendet werden, unabhängig davon, ob das [**SplitButton**](windowsribbon-element-splitbutton.md) -Steuerelement in der Multifunktionsleiste, in der QAT oder in **contextpopup** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b5cd9-151">In this case, the Paste Command handlers can be used whether the [**SplitButton**](windowsribbon-element-splitbutton.md) control appears in the Ribbon, the QAT, or the **ContextPopup**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b5cd9-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5cd9-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5cd9-153">Einführung in das Windows-Menü Band Framework</span><span class="sxs-lookup"><span data-stu-id="b5cd9-153">Introducing the Windows Ribbon Framework</span></span>](windowsribbon-introduction.md)
</dt> <dt>

[<span data-ttu-id="b5cd9-154">Erstellen einer Menü Bandanwendung</span><span class="sxs-lookup"><span data-stu-id="b5cd9-154">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="b5cd9-155">Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup</span><span class="sxs-lookup"><span data-stu-id="b5cd9-155">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 