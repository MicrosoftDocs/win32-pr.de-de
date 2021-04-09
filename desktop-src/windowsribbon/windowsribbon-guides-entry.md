---
title: Entwickler Handbücher für Windows Ribbon Framework
description: Die in diesem Abschnitt enthaltenen Themen beschreiben bestimmte Aspekte des Windows-Menüband-Frameworks.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Windows-Menüband, Framework
- Menüband, Framework
- Windows-Menüband, Entwickler Handbücher
- Menüband, Entwickler Handbücher
- Entwickler Handbücher für Windows-Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b6e88045efdd31384d99370fdd9bb9cb264598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102155"
---
# <a name="windows-ribbon-framework-developer-guides"></a><span data-ttu-id="9aeb4-108">Entwickler Handbücher für Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="9aeb4-108">Windows Ribbon Framework Developer Guides</span></span>

<span data-ttu-id="9aeb4-109">Die in diesem Abschnitt enthaltenen Themen beschreiben bestimmte Aspekte des Windows-Menüband-Frameworks.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-109">The topics contained in this section describe specific aspects of the Windows Ribbon framework.</span></span>

## <a name="basics"></a><span data-ttu-id="9aeb4-110">Grundlagen</span><span class="sxs-lookup"><span data-stu-id="9aeb4-110">Basics</span></span>

[<span data-ttu-id="9aeb4-111">Erstellen einer Menü Bandanwendung</span><span class="sxs-lookup"><span data-stu-id="9aeb4-111">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)

<span data-ttu-id="9aeb4-112">Damit das Windows-Menüband-Framework die Menüband-Markup Datei verwendet, muss die Markup Datei in eine Ressourcen Datei im Binärformat kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-112">For the Windows Ribbon framework to consume the Ribbon markup file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="9aeb4-113">Ein dedizierter Menüband-Markup Compiler, der UI-Befehls Compiler (UICC), ist zu diesem Zweck im Microsoft Windows Software Development Kit (SDK) (7,0 oder höher) enthalten.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-113">A dedicated Ribbon markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="9aeb4-114">Neben der Kompilierung der Binärversion des Menüband-Markups generiert UICC eine ID-Definitions Header Datei (. h), die alle Markup Elemente für die Menüband-Host Anwendung und eine Ressourcen Datei (. RC) zur Verfügung stellt, mit der Bild-und Zeichen folgen Ressourcen zur Buildzeit mit der Host Anwendung verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-114">In addition to compiling the binary version of the Ribbon markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="9aeb4-115">Migrieren zum Windows-Menü Band Framework</span><span class="sxs-lookup"><span data-stu-id="9aeb4-115">Migrating to the Windows Ribbon Framework</span></span>](ribbon-migration.md)

<span data-ttu-id="9aeb4-116">Eine Anwendung, die auf herkömmlichen Menüs, Symbolleisten und Dialogfeldern basiert, kann auf die umfangreiche, dynamische und Kontext gesteuerte Benutzeroberfläche (UI) des befehlssystems des Multifunktionsleisten-Frameworks migriert werden.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-116">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven user interface (UI) of the Ribbon framework Command system.</span></span> <span data-ttu-id="9aeb4-117">Dies ist eine einfache und effektive Möglichkeit, um die Anwendung zu modernisieren und zu beleben und gleichzeitig die Barrierefreiheit, die Benutzerfreundlichkeit und die Auffindbarkeit ihrer Funktionalität zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-117">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

[<span data-ttu-id="9aeb4-118">Grundlegendes zu Befehlen und Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="9aeb4-118">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)

<span data-ttu-id="9aeb4-119">Die Trennung der Logik von der Präsentation ist die Entwurfs Philosophie, die das Befehls Präsentationssystem des Multifunktionsleisten-Frameworks inspiriert – ein System, das auf einem Entwurfsmuster basiert, in dem Funktionalität und Verhalten unabhängig von den Steuerelementen implementiert werden, die diese Funktionalität verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-119">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

## <a name="user-interface"></a><span data-ttu-id="9aeb4-120">Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="9aeb4-120">User Interface</span></span>

[<span data-ttu-id="9aeb4-121">Angeben von Menüband-Bild Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9aeb4-121">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)

<span data-ttu-id="9aeb4-122">Als umfassendes Befehls Präsentationssystem ist das Menüband-Framework für die Unterstützung von Bild Ressourcen in der Multifunktionsleisten-Benutzeroberfläche (UI) konzipiert.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-122">As a rich command presentation system, the Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="9aeb4-123">Alle Bild Ressourcen werden im [Menüband-Markup](windowsribbon-schema.md) deklariert oder von einer Menüband-Host Anwendung abgefragt.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-123">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="9aeb4-124">Für Windows 8 und höher unterstützt das Menüband-Framework die folgenden Grafikformate: 32-Bit-ARGB-Bitmap-Dateien (BMP) und Portable Network Graphics-Dateien (PNG) mit Transparenz.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-124">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="9aeb4-125">Für Windows 7 und früher müssen Bild Ressourcen dem standardmäßigen BMP-Grafikformat entsprechen, das in Windows verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-125">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

[<span data-ttu-id="9aeb4-126">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="9aeb4-126">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)

<span data-ttu-id="9aeb4-127">Steuerelemente, die in der Multifunktionsleisten-Befehlsleiste gehostet werden, unterliegen Layoutregeln, die vom Menüband-Framework erzwungen werden, und basieren auf einer Kombination aus Standardverhalten und Layoutvorlagen (sowohl Framework-definiert als auch Benutzer definiert), wie im Menü Band Markup</span><span class="sxs-lookup"><span data-stu-id="9aeb4-127">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="9aeb4-128">Diese Regeln definieren das Verhalten des adaptiven Layouts des Multifunktionsleisten-Frameworks, das beeinflussen, wie die Steuerelemente in der Befehlsleiste zur Laufzeit an verschiedene Menü Bandgrößen angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-128">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

[<span data-ttu-id="9aeb4-129">Arbeiten mit Galerien</span><span class="sxs-lookup"><span data-stu-id="9aeb4-129">Working with Galleries</span></span>](ribbon-controls-galleries.md)

<span data-ttu-id="9aeb4-130">Das Menüband-Framework bietet Entwicklern ein stabiles und konsistentes Modell für die Verwaltung dynamischer Inhalte über eine Vielzahl von Sammlungs basierten Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-130">The Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="9aeb4-131">Durch das anpassen und Neukonfigurieren der Multifunktionsleisten-Benutzeroberfläche ermöglichen diese dynamischen Steuerelemente dem Framework, auf die Benutzerinteraktion sowohl in der Host Anwendung als auch auf dem Menüband selbst zu reagieren und die Flexibilität für verschiedene Laufzeitumgebungen zu bieten.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-131">By adapting and reconfiguring the Ribbon user interface (UI), these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

[<span data-ttu-id="9aeb4-132">Anzeigen kontextbezogener Registerkarten</span><span class="sxs-lookup"><span data-stu-id="9aeb4-132">Displaying Contextual Tabs</span></span>](ribbon-contextualtabs.md)

<span data-ttu-id="9aeb4-133">In einer Multifunktionsleisten-Framework-Anwendung ist eine Kontext Registerkarte ein ausgeblendetes [Register](windowsribbon-controls-tab.md) Karten-Steuerelement, das in der Registerkarten Zeile angezeigt wird, wenn ein Objekt im Anwendungs Arbeitsbereich (z. b. ein Bild) ausgewählt oder markiert</span><span class="sxs-lookup"><span data-stu-id="9aeb4-133">In a Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

[<span data-ttu-id="9aeb4-134">Neukonfigurieren des Menübands mit Anwendungsmodi</span><span class="sxs-lookup"><span data-stu-id="9aeb4-134">Reconfiguring the Ribbon with Application Modes</span></span>](ribbon-applicationmodes.md)

<span data-ttu-id="9aeb4-135">Das Menüband-Framework unterstützt die dynamische Neukonfiguration und das verfügbar machen von Kernelementen der Menüband-Benutzeroberfläche (User Interface, UI) zur Laufzeit basierend auf dem Zustand der Anwendung (auch als Kontext bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="9aeb4-135">The Ribbon framework supports the dynamic reconfiguring and exposing of core elements of the Ribbon user interface (UI) at run time, based on the application's state (also referred to as context).</span></span> <span data-ttu-id="9aeb4-136">Die verschiedenen Zustände, die von einer Anwendung unterstützt werden, werden als Anwendungsmodi bezeichnet und mit bestimmten Elementen im Markup verknüpft.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-136">Declared and associated with specific elements in markup, the various states supported by an application are referred to as application modes.</span></span>

[<span data-ttu-id="9aeb4-137">Anpassen von Menü Band Farben</span><span class="sxs-lookup"><span data-stu-id="9aeb4-137">Customizing Ribbon Colors</span></span>](ribbon-color.md)

<span data-ttu-id="9aeb4-138">Das Menüband-Framework macht eine Reihe von Farbeigenschaften verfügbar, die es einer Anwendung ermöglichen, die Darstellung verschiedener Benutzeroberflächen Elemente der Multifunktionsleiste zur Laufzeit anzupassen.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-138">The Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon user interface (UI) elements at run time.</span></span>

[<span data-ttu-id="9aeb4-139">Anzeigen des Menübands</span><span class="sxs-lookup"><span data-stu-id="9aeb4-139">Displaying the Ribbon</span></span>](ribbon-visibility.md)

<span data-ttu-id="9aeb4-140">Das Menüband-Framework macht eine Reihe von Eigenschaften verfügbar, die es einer Anwendung ermöglichen, anzugeben, wie die Menüband-Benutzeroberfläche zur Laufzeit angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-140">The Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon user interface (UI) is displayed at run time.</span></span>

## <a name="management"></a><span data-ttu-id="9aeb4-141">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="9aeb4-141">Management</span></span>

[<span data-ttu-id="9aeb4-142">Beibehalten des Multifunktionsleisten Status</span><span class="sxs-lookup"><span data-stu-id="9aeb4-142">Persisting Ribbon State</span></span>](ribbon-statepersistence.md)

<span data-ttu-id="9aeb4-143">Das Windows Ribon-Framework (Menüband) bietet die Möglichkeit, den Zustand einer Vielzahl von Benutzereinstellungen und-Einstellungen über Anwendungs Sitzungen hinweg beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-143">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

[<span data-ttu-id="9aeb4-144">Lauschen auf Menü Band Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9aeb4-144">Listening for Ribbon Events</span></span>](listening-for-ribbon-events.md)

<span data-ttu-id="9aeb4-145">Das Menüband Framework verwendet die Infrastruktur der [Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw)](../etw/event-tracing-portal.md) , um Entwicklern zu ermöglichen, zu erfahren, wie Benutzer mit dem Menüband Ihrer Anwendung</span><span class="sxs-lookup"><span data-stu-id="9aeb4-145">The Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="markup-compiler"></a><span data-ttu-id="9aeb4-146">Markup Compiler</span><span class="sxs-lookup"><span data-stu-id="9aeb4-146">Markup Compiler</span></span>

[<span data-ttu-id="9aeb4-147">Kompilieren von Menü Band Markup</span><span class="sxs-lookup"><span data-stu-id="9aeb4-147">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)

<span data-ttu-id="9aeb4-148">Damit das Menüband-Framework die [Menüband-Markup](windowsribbon-schema.md) Datei verwendet, muss die Markup Datei in eine Ressourcen Datei im Binärformat kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-148">For the Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="9aeb4-149">Ein dedizierter Markup Compiler, der UI-Befehls Compiler (UICC), ist zu diesem Zweck im Microsoft Windows Software Development Kit (SDK) (7,0 oder höher) enthalten.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-149">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="9aeb4-150">Zusätzlich zum Kompilieren der Binärversion des Markups generiert das UICC eine ID-Definitions Header Datei (. h), die alle Markup Elemente für die Menüband-Host Anwendung und eine Ressourcen Datei (. RC) verfügbar macht, mit der Bild-und Zeichen folgen Ressourcen zur Buildzeit mit der Host Anwendung verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="9aeb4-150">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="9aeb4-151">Grundlegendes zu Markup Compiler-Meldungen</span><span class="sxs-lookup"><span data-stu-id="9aeb4-151">Understanding Markup Compiler Messages</span></span>](windowsribbon-compilationerrors.md)

<span data-ttu-id="9aeb4-152">Der Markup Compiler des Windows-Menüband-Frameworks (Menüband), der UI-Befehls Compiler (UICC.exe), überprüft das Menüband-Markup sowohl mit dem Menüband-Schema als auch mit einem zusätzlichen Regelsatz, der durch das Menüband</span><span class="sxs-lookup"><span data-stu-id="9aeb4-152">The Windows Ribbon framework (Ribbon) markup compiler, UI Command Compiler (UICC.exe), validates the Ribbon markup against both the Ribbon schema and an additional set of rules defined by the Ribbon framework.</span></span>

 

 