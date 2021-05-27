---
title: Übersicht über DWriteCore
description: DWriteCore ist die Project Reunion-Implementierung von DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: c619b74cf334218813a74e63cca6d5fab400e563
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550295"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="8fd17-105">Übersicht über DWriteCore</span><span class="sxs-lookup"><span data-stu-id="8fd17-105">DWriteCore overview</span></span>

<span data-ttu-id="8fd17-106">DWriteCore ist die [Project Reunion-Implementierung](/windows/apps/project-reunion/) von [DirectWrite (DirectWrite](./direct-write-portal.md) ist die DirectX-API für hochwertiges Textrendering, auflösungsunabhängige Konturschriftarten und Vollständige Unicode-Text- und Layoutunterstützung).</span><span class="sxs-lookup"><span data-stu-id="8fd17-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md) (DirectWrite is the DirectX API for high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support).</span></span> <span data-ttu-id="8fd17-107">DWriteCore ist eine Form von DirectWrite, die unter Windows-Versionen bis Windows 10, Version 1809 (10.0; Build 17763), und öffnet ihnen die Tür für die plattformübergreifende Verwendung.</span><span class="sxs-lookup"><span data-stu-id="8fd17-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 10, version 1809 (10.0; Build 17763), and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="8fd17-108">In diesem Einführungsthema wird beschrieben, was DWriteCore ist, und es wird gezeigt, wie Sie DWriteCore in Ihrer Entwicklungsumgebung installieren und damit programmieren.</span><span class="sxs-lookup"><span data-stu-id="8fd17-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="8fd17-109">Das Wertversprechen von DWriteCore</span><span class="sxs-lookup"><span data-stu-id="8fd17-109">The value proposition of DWriteCore</span></span>

<span data-ttu-id="8fd17-110">[DirectWrite](./direct-write-portal.md) selbst unterstützt ein umfangreiches Array von Features, wodurch es für die meisten Apps unter Windows zum Tool der Wahl beim Rendern von Schriftarten wird, unabhängig davon, ob dies über direkte Aufrufe oder &mdash; [über Direct2D erfolgt.](../direct2d/direct2d-portal.md)</span><span class="sxs-lookup"><span data-stu-id="8fd17-110">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="8fd17-111">DirectWrite umfasst ein geräteunabhängiges Textlayoutsystem, qualitativ [hochwertiges Microsoft ClearType-Textrendering,](/typography/cleartype/) hardwarebeschleunigten Text, Text mit mehreren Formaten, erweiterte [OpenType®](/typography/opentype/) Typografiefeatures, Unterstützung für breite Sprache und [GDI-kompatibles](../gdi/windows-gdi.md)Layout und Rendering.</span><span class="sxs-lookup"><span data-stu-id="8fd17-111">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="8fd17-112">DirectWrite ist seit Windows Vista SP2 verfügbar und hat sich im Laufe der Jahre weiterentwickelt, um erweiterte Features wie variable Schriftarten zu enthalten, mit denen Sie Stile, Gewichtungen und andere Attribute auf eine Schriftart mit nur einer Schriftartressource anwenden können.</span><span class="sxs-lookup"><span data-stu-id="8fd17-112">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables you to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="8fd17-113">Aufgrund der langen Lebensdauer von DirectWrite haben Fortschritte bei der Entwicklung jedoch tendenziell ältere Versionen von Windows zurückgelassen.</span><span class="sxs-lookup"><span data-stu-id="8fd17-113">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="8fd17-114">Darüber hinaus ist der Status von DirectWrite als führende Textrenderingtechnologie nur auf Windows beschränkt, wodurch plattformübergreifende Anwendungen entweder ihren eigenen Textrenderingstapel schreiben oder sich auf Lösungen von Drittanbietern verlassen können.</span><span class="sxs-lookup"><span data-stu-id="8fd17-114">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="8fd17-115">DWriteCore löst die grundlegenden Probleme des Verwaistens von Versionsfeatures und der plattformübergreifenden Kompatibilität, indem die Bibliothek aus dem System entfernt wird und alle möglichen unterstützten Endpunkte als Ziel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fd17-115">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="8fd17-116">Zu diesem Zweck haben wir DWriteCore in Project Reunion integriert.</span><span class="sxs-lookup"><span data-stu-id="8fd17-116">To that end, we've integrated DWriteCore into Project Reunion.</span></span>

<span data-ttu-id="8fd17-117">DWriteCore bietet Ihnen als Entwickler in Project Reunion hauptsächlich Den Zugriff auf viele (und schließlich alle) DirectWrite-Features.</span><span class="sxs-lookup"><span data-stu-id="8fd17-117">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to many (and eventually all) DirectWrite features.</span></span> <span data-ttu-id="8fd17-118">Alle Features von DWriteCore funktionieren auf allen Downlevelversionen gleich, ohne dass es zu Abweichungen hinsichtlich der Features kommt, die für welche Versionen funktionieren können.</span><span class="sxs-lookup"><span data-stu-id="8fd17-118">All features of DWriteCore will function the same on all down-level versions without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="8fd17-119">Die DWriteCore-Demo-App &mdash; DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="8fd17-119">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="8fd17-120">DWriteCore wird anhand der [Beispiel-App DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) veranschaulicht, die Sie jetzt herunterladen und untersuchen können.</span><span class="sxs-lookup"><span data-stu-id="8fd17-120">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="8fd17-121">Erste Schritte mit DWriteCore</span><span class="sxs-lookup"><span data-stu-id="8fd17-121">Get started with DWriteCore</span></span>

<span data-ttu-id="8fd17-122">DWriteCore ist Teil von [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span><span class="sxs-lookup"><span data-stu-id="8fd17-122">DWriteCore is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="8fd17-123">In diesem Abschnitt wird beschrieben, wie Sie Ihre Entwicklungsumgebung für die Programmierung mit DWriteCore einrichten.</span><span class="sxs-lookup"><span data-stu-id="8fd17-123">This section describes how to set up your development environment for programming with DWriteCore.</span></span>

### <a name="install-the-project-reunion-05-vsix"></a><span data-ttu-id="8fd17-124">Installieren von Project Reunion 0.5 VSIX</span><span class="sxs-lookup"><span data-stu-id="8fd17-124">Install the Project Reunion 0.5 VSIX</span></span>

<span data-ttu-id="8fd17-125">Klicken Sie in Visual Studio auf  >  **Erweiterungen Erweiterungen verwalten,** suchen Sie nach *Project Reunion*, und laden Sie die Erweiterung Project Reunion herunter.</span><span class="sxs-lookup"><span data-stu-id="8fd17-125">In Visual Studio, click **Extensions** > **Manage Extensions**, search for *Project Reunion*, and download the Project Reunion extension.</span></span> <span data-ttu-id="8fd17-126">Schließen Sie Visual Studio, öffnen Sie sie erneut, und befolgen Sie die Anweisungen, um die Erweiterung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="8fd17-126">Close and reopen Visual Studio, and follow the prompts to install the extension.</span></span>

<span data-ttu-id="8fd17-127">Weitere Informationen finden Sie unter [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)und [Einrichten Ihrer Entwicklungsumgebung (für Project Reunion).](/windows/apps/project-reunion/get-started-with-project-reunion#set-up-your-development-environment)</span><span class="sxs-lookup"><span data-stu-id="8fd17-127">For more info, see [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0), and [Set up your development environment (for Project Reunion)](/windows/apps/project-reunion/get-started-with-project-reunion#set-up-your-development-environment).</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="8fd17-128">Erstellen eines neuen Projekts</span><span class="sxs-lookup"><span data-stu-id="8fd17-128">Create a new project</span></span>

<span data-ttu-id="8fd17-129">Erstellen Sie in Visual Studio ein neues Projekt aus der Projektvorlage **Leere App, gepackt (WinUI 3 in Desktop).**</span><span class="sxs-lookup"><span data-stu-id="8fd17-129">In Visual Studio, create a new project from the **Blank App, Packaged (WinUI 3 in Desktop)** project template.</span></span> <span data-ttu-id="8fd17-130">Sie finden diese Projektvorlage, indem Sie sprache auswählen: *C++*; platform: *Project Reunion*; Projekttyp: *Desktop*.</span><span class="sxs-lookup"><span data-stu-id="8fd17-130">You can find that project template by choosing language: *C++*; platform: *Project Reunion*; project type: *Desktop*.</span></span>

<span data-ttu-id="8fd17-131">Weitere Informationen finden Sie unter [Erste Schritte mit WinUI 3 für Desktop-Apps.](/windows/apps/winui/winui3/get-started-winui3-for-desktop)</span><span class="sxs-lookup"><span data-stu-id="8fd17-131">For more info, see [Get started with WinUI 3 for desktop apps](/windows/apps/winui/winui3/get-started-winui3-for-desktop).</span></span>

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a><span data-ttu-id="8fd17-132">Installieren des NuGet-Pakets Microsoft.ProjectReunion.DWrite</span><span class="sxs-lookup"><span data-stu-id="8fd17-132">Install the Microsoft.ProjectReunion.DWrite NuGet package</span></span>

<span data-ttu-id="8fd17-133">Klicken Sie in Visual Studio  auf \> **Projekt NuGet-Pakete verwalten...** Durchsuchen , geben Oder fügen Sie \>  **Microsoft.ProjectReunion.DWrite** in das Suchfeld ein, wählen Sie das Element in den Suchergebnissen aus, und klicken Sie dann auf **Installieren,** um das Paket für dieses Projekt zu installieren.</span><span class="sxs-lookup"><span data-stu-id="8fd17-133">In Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.ProjectReunion.DWrite** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a><span data-ttu-id="8fd17-134">Alternativ können Sie mit der Beispiel-App DWriteCoreGallery beginnen.</span><span class="sxs-lookup"><span data-stu-id="8fd17-134">Alternatively, begin with the DWriteCoreGallery sample app</span></span>

<span data-ttu-id="8fd17-135">Alternativ können Sie mit DWriteCore programmieren, indem Sie mit dem Beispiel-App-Projekt [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) beginnen und Ihre Entwicklung auf diesem Projekt basieren.</span><span class="sxs-lookup"><span data-stu-id="8fd17-135">Alternatively, you can program with DWriteCore by beginning with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span> <span data-ttu-id="8fd17-136">Anschließend können Sie beliebigen vorhandenen Quellcode (oder dateien) aus diesem Beispielprojekt entfernen und dem Projekt neuen Quellcode (oder neue Dateien) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8fd17-136">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span>

### <a name="use-dwritecore-in-your-project"></a><span data-ttu-id="8fd17-137">Verwenden von DWriteCore in Ihrem Projekt</span><span class="sxs-lookup"><span data-stu-id="8fd17-137">Use DWriteCore in your project</span></span>

<span data-ttu-id="8fd17-138">Weitere Informationen zum Programmieren mit DWriteCore finden Sie im Abschnitt Programmieren mit [DWriteCore](#programming-with-dwritecore) weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="8fd17-138">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="8fd17-139">Die Releasephasen von DWriteCore</span><span class="sxs-lookup"><span data-stu-id="8fd17-139">The release phases of DWriteCore</span></span>

<span data-ttu-id="8fd17-140">Das Portieren von DirectWrite zu DWriteCore ist ein ausreichend großes Projekt, das mehrere Windows-Releasezyklen umfassen kann.</span><span class="sxs-lookup"><span data-stu-id="8fd17-140">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="8fd17-141">Dieses Projekt ist in Phasen unterteilt, die jeweils einem Teil der In einem Release bereitgestellten Funktionalität entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8fd17-141">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="8fd17-142">Features in der aktuellen Version von DWriteCore</span><span class="sxs-lookup"><span data-stu-id="8fd17-142">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="8fd17-143">Die derzeit verfügbare Version von DWriteCore ist Teil von [Project Reunion 0.5.](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)</span><span class="sxs-lookup"><span data-stu-id="8fd17-143">The version of DWriteCore currently available is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="8fd17-144">Es enthält die grundlegenden Tools, die Sie als Entwickler benötigen, um DWriteCore zu nutzen, einschließlich der folgenden Features.</span><span class="sxs-lookup"><span data-stu-id="8fd17-144">It contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="8fd17-145">Schriftartenenumeration.</span><span class="sxs-lookup"><span data-stu-id="8fd17-145">Font enumeration.</span></span>
- <span data-ttu-id="8fd17-146">Schriftart-API.</span><span class="sxs-lookup"><span data-stu-id="8fd17-146">Font API.</span></span>
- <span data-ttu-id="8fd17-147">Gestaltung.</span><span class="sxs-lookup"><span data-stu-id="8fd17-147">Shaping.</span></span>
- <span data-ttu-id="8fd17-148">Rendering-APIs auf niedriger Ebene.</span><span class="sxs-lookup"><span data-stu-id="8fd17-148">Low-level rendering APIs.</span></span> <span data-ttu-id="8fd17-149">Dies ist teilweise in der aktuellen Phase DWriteCore funktioniert nicht mit &mdash; [Direct2D,](../direct2d/direct2d-portal.md)aber Sie können [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) und [**IDWriteBitmapRenderTarget verwenden.**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)</span><span class="sxs-lookup"><span data-stu-id="8fd17-149">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="8fd17-150">Grundlegende Textlayoutfunktionalität.</span><span class="sxs-lookup"><span data-stu-id="8fd17-150">Basic text layout functionality.</span></span>
- <span data-ttu-id="8fd17-151">Textrendering-APIs.</span><span class="sxs-lookup"><span data-stu-id="8fd17-151">Text-rendering APIs.</span></span>
- <span data-ttu-id="8fd17-152">Bitmaprenderingziel.</span><span class="sxs-lookup"><span data-stu-id="8fd17-152">Bitmap render target.</span></span>
- <span data-ttu-id="8fd17-153">Farbschriftarten.</span><span class="sxs-lookup"><span data-stu-id="8fd17-153">Color fonts.</span></span>
- <span data-ttu-id="8fd17-154">Verschiedene Optimierungen (Bereinigung des Schriftartcaches, In-Memory-Schriftartlademodul und so weiter).</span><span class="sxs-lookup"><span data-stu-id="8fd17-154">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="8fd17-155">Ein Bannerfeature sind Farbschriftarten.</span><span class="sxs-lookup"><span data-stu-id="8fd17-155">A banner feature is color fonts.</span></span> <span data-ttu-id="8fd17-156">MitHilfe von Farbschriftarten können Sie Ihre Schriftarten mit komplexeren Farbfunktionen rendern, die über einfache Einzelfarben hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="8fd17-156">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="8fd17-157">Farbschriftarten sind z. B. die Möglichkeit, Emoji- und Symbolsymbolschriftarten zu rendern (letzteres wird z. B. von Office verwendet).</span><span class="sxs-lookup"><span data-stu-id="8fd17-157">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="8fd17-158">Farbschriftarten wurden erstmals in Windows 8.1 eingeführt, aber das Feature wurde in Windows 10 Version 1607 (Anniversary Update) stark erweitert.</span><span class="sxs-lookup"><span data-stu-id="8fd17-158">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="8fd17-159">Die Arbeit an der Bereinigung des Schriftartcaches und des In-Memory-Schriftartlademoduls ermöglicht ein schnelleres Laden von Schriftarten und Arbeitsspeicherverbesserungen.</span><span class="sxs-lookup"><span data-stu-id="8fd17-159">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="8fd17-160">Mit diesen Features können Sie sofort damit beginnen, einige der modernen Kernfunktionen von DirectWrite &mdash; zu nutzen, z. B. variable Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="8fd17-160">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts.</span></span> <span data-ttu-id="8fd17-161">Variable Schriftarten sind eines der wichtigsten Features für DirectWrite-Kunden.</span><span class="sxs-lookup"><span data-stu-id="8fd17-161">Variable fonts are one of the most important features for DirectWrite customers.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="8fd17-162">Unsere Einladung für Sie als DirectWrite-Entwickler</span><span class="sxs-lookup"><span data-stu-id="8fd17-162">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="8fd17-163">DWriteCore wird zusammen mit anderen Project Reunion-Komponenten mit Entwicklerfeedback entwickelt.</span><span class="sxs-lookup"><span data-stu-id="8fd17-163">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="8fd17-164">Wir laden Sie ein, mit dem Erkunden von DWriteCore zu beginnen und Einblicke oder Anforderungen in die Featureentwicklung in unserem [GitHub-Repository Project Reunion](https://github.com/microsoft/ProjectReunion/)bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8fd17-164">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="8fd17-165">Programmieren mit DWriteCore</span><span class="sxs-lookup"><span data-stu-id="8fd17-165">Programming with DWriteCore</span></span>

<span data-ttu-id="8fd17-166">Genau wie bei [DirectWrite programmieren](./direct-write-portal.md)Sie mit DWriteCore über die COM-Light-API über die [**IDWriteFactory-Schnittstelle.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)</span><span class="sxs-lookup"><span data-stu-id="8fd17-166">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="8fd17-167">Um DWriteCore zu verwenden, muss die Headerdatei eingeschlossen `dwrite_core.h` werden.</span><span class="sxs-lookup"><span data-stu-id="8fd17-167">To use DWriteCore, it's necessary to include the `dwrite_core.h` header file.</span></span>

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

<span data-ttu-id="8fd17-168">Die `dwrite_core.h` Headerdatei definiert zuerst das Token *DWRITE_CORE* und enthält dann die `dwrite_3.h` Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="8fd17-168">The `dwrite_core.h` header file first defines the token *DWRITE_CORE*, and then it includes the `dwrite_3.h` header file.</span></span> <span data-ttu-id="8fd17-169">Das *DWRITE_CORE* Token ist wichtig, da es alle nachfolgend enthaltenen Header anleitet, ihnen alle DirectWrite-APIs zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="8fd17-169">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="8fd17-170">Sobald Ihr Projekt enthalten `dwrite_core.h` ist, können Sie code, build und run schreiben.</span><span class="sxs-lookup"><span data-stu-id="8fd17-170">Once your project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="8fd17-171">APIs, die neu oder anders für DWriteCore sind</span><span class="sxs-lookup"><span data-stu-id="8fd17-171">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="8fd17-172">Die Oberfläche der DWriteCore-API ist größtenteils identisch mit der Oberfläche für [DirectWrite.](/windows/win32/api/_directwrite/)</span><span class="sxs-lookup"><span data-stu-id="8fd17-172">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="8fd17-173">Es gibt jedoch eine kleine Anzahl neuer APIs, die sich derzeit nur in DWriteCore befinden.</span><span class="sxs-lookup"><span data-stu-id="8fd17-173">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-factory-object"></a><span data-ttu-id="8fd17-174">Erstellen eines Factoryobjekts</span><span class="sxs-lookup"><span data-stu-id="8fd17-174">Create a factory object</span></span>

<span data-ttu-id="8fd17-175">Die [**freie DWriteCoreCreateFactory-Funktion**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) erstellt ein Factoryobjekt, das für die nachfolgende Erstellung einzelner DWriteCore-Objekte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fd17-175">The [**DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) free function creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

<span data-ttu-id="8fd17-176">**DWriteCoreCreateFactory** ist funktionell identisch mit der [DWriteCreateFactory-Funktion,](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) die von der Systemversion von DirectWrite exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8fd17-176">**DWriteCoreCreateFactory** is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="8fd17-177">Die DWriteCore-Funktion hat einen anderen Namen, um Mehrdeutigkeiten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="8fd17-177">The DWriteCore function has a different name to avoid ambiguity.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="8fd17-178">Erstellen eines eingeschränkten Factoryobjekts</span><span class="sxs-lookup"><span data-stu-id="8fd17-178">Create a restricted factory object</span></span>

<span data-ttu-id="8fd17-179">Die [**DWRITE_FACTORY_TYPE-Enumeration**](./dwrite/ne-dwrite-dwrite_factory_type.md) verfügt über eine neue Konstante &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, die eine eingeschränkte Factory angibt.</span><span class="sxs-lookup"><span data-stu-id="8fd17-179">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_ISOLATED2**, indicating a restricted factory.</span></span> <span data-ttu-id="8fd17-180">Eine eingeschränkte Factory ist stärker gesperrt als eine isolierte Factory.</span><span class="sxs-lookup"><span data-stu-id="8fd17-180">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="8fd17-181">Es interagiert in irgendeiner Weise nicht mit einem prozessübergreifenden oder beständigen Schriftartcache.</span><span class="sxs-lookup"><span data-stu-id="8fd17-181">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="8fd17-182">Darüber hinaus enthält die von dieser Factory zurückgegebene Auflistung von Systemschriftarten nur bekannte Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="8fd17-182">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="8fd17-183">So können Sie DWRITE_FACTORY_TYPE_ISOLATED2 verwenden, um **ein** eingeschränktes Factoryobjekt zu erstellen, wenn Sie die freie [**DWriteCoreCreateFactory-Funktion**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8fd17-183">Here's how you can use **DWRITE_FACTORY_TYPE_ISOLATED2** to create a restricted factory object when you call the [**DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) free function.</span></span>

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

<span data-ttu-id="8fd17-184">Wenn Sie **DWRITE_FACTORY_TYPE_ISOLATED2** an eine ältere Version von DirectWrite übergeben, die sie nicht unterstützt, gibt **DWriteCreateFactory** **E_INVALIDARG.**</span><span class="sxs-lookup"><span data-stu-id="8fd17-184">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="8fd17-185">Zeichnen von Glyphen in eine Systemspeicherbitmap</span><span class="sxs-lookup"><span data-stu-id="8fd17-185">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="8fd17-186">DirectWrite verfügt über eine Bitmap-Renderzielschnittstelle, die das Rendern von Glyphen in eine Bitmap im Systemspeicher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8fd17-186">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="8fd17-187">Derzeit besteht die einzige Möglichkeit, zugriff auf die zugrunde liegenden Pixeldaten zu erhalten, in der Verwendung von GDI, sodass die API nicht plattformübergreifend verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8fd17-187">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="8fd17-188">Dies lässt sich leicht beheben, indem eine Methode zum Abrufen der Pixeldaten hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8fd17-188">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="8fd17-189">DWriteCore führt daher die [**IDWriteBitmapRenderTarget2-Schnittstelle**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) und deren [**Methode IDWriteBitmapRenderTarget2::GetBitmapData ein.**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md)</span><span class="sxs-lookup"><span data-stu-id="8fd17-189">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="8fd17-190">Diese Methode akzeptiert einen Parameter des Typs (Zeiger auf) DWRITE_BITMAP_DATA_BGRA32 [**,**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md)bei dem es sich um eine neue Struktur handelt.</span><span class="sxs-lookup"><span data-stu-id="8fd17-190">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="8fd17-191">Ihre Anwendung erstellt ein Bitmaprenderingziel durch Aufrufen von [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="8fd17-191">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="8fd17-192">Unter Windows kapselt ein Bitmaprenderingziel einen GDI-Speicherdomänencontroller mit einer in ihm ausgewählten geräteunabhängigen GDI-Bitmap (DEVICE-Independent Bitmap, DIB).</span><span class="sxs-lookup"><span data-stu-id="8fd17-192">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="8fd17-193">[IDWriteBitmapRenderTarget::D rawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) rendert Glyphen im DIB.</span><span class="sxs-lookup"><span data-stu-id="8fd17-193">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="8fd17-194">DirectWrite rendert die Glyphen selbst, ohne GDI zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="8fd17-194">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="8fd17-195">Ihre Anwendung kann dann den **HDC** aus dem Bitmaprenderziel abrufen und [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) verwenden, um die Pixel in ein **HDC-Fenster** zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="8fd17-195">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="8fd17-196">Auf Nicht-Windows-Plattformen kann Ihre Anwendung weiterhin ein Bitmaprenderingziel erstellen, kapselt aber einfach ein Systemspeicherarray ohne **HDC** und ohne DIB.</span><span class="sxs-lookup"><span data-stu-id="8fd17-196">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="8fd17-197">Ohne **HDC** muss es eine andere Möglichkeit für Ihre Anwendung geben, die Bitmappixel abzurufen, damit sie sie kopieren oder anderweitig verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="8fd17-197">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="8fd17-198">Selbst unter Windows ist es manchmal nützlich, die tatsächlichen Pixeldaten abzurufen, und wir zeigen die aktuelle Vorgehensweise im folgenden Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="8fd17-198">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="8fd17-199">Andere API-Unterschiede zwischen DWriteCore und DirectWrite</span><span class="sxs-lookup"><span data-stu-id="8fd17-199">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="8fd17-200">Es gibt einige APIs, die entweder nur Stubs sind oder sich auf Nicht-Windows-Plattformen etwas anders verhalten.</span><span class="sxs-lookup"><span data-stu-id="8fd17-200">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="8fd17-201">Beispielsweise gibt [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) **E_NOTIMPL** auf Nicht-Windows-Plattformen zurück, da es kein **HDC** ohne [GDI](../gdi/windows-gdi.md)gibt.</span><span class="sxs-lookup"><span data-stu-id="8fd17-201">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="8fd17-202">Und schließlich gibt es bestimmte andere Windows-APIs, die in der Regel zusammen mit DirectWrite verwendet werden (Direct2D ist ein bedeutendes Beispiel).</span><span class="sxs-lookup"><span data-stu-id="8fd17-202">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="8fd17-203">Derzeit können Direct2D und DWriteCore jedoch nicht zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8fd17-203">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="8fd17-204">Wenn Sie beispielsweise ein [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mit DWriteCore erstellen und es an [**D2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)übergeben, tritt bei diesem Aufruf ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="8fd17-204">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>