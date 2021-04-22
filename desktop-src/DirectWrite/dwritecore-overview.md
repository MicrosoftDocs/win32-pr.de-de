---
title: Übersicht über DWriteCore
description: DWriteCore ist die Project Reunion-Implementierung von DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 04/21/2021
ms.openlocfilehash: 27a34656ce28a65267bd098974b4df9003a80e17
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881839"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="33801-105">Übersicht über DWriteCore</span><span class="sxs-lookup"><span data-stu-id="33801-105">DWriteCore overview</span></span>

<span data-ttu-id="33801-106">DWriteCore ist die [Project Reunion-Implementierung](/windows/apps/project-reunion/) von [DirectWrite (DirectWrite](./direct-write-portal.md) ist die DirectX-API für hochwertiges Textrendering, auflösungsunabhängige Konturschriftarten und Vollständige Unicode-Text- und Layoutunterstützung).</span><span class="sxs-lookup"><span data-stu-id="33801-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md) (DirectWrite is the DirectX API for high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support).</span></span> <span data-ttu-id="33801-107">DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="33801-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="33801-108">In diesem Einführungsthema wird beschrieben, was DWriteCore ist, und es wird gezeigt, wie Sie DWriteCore in Ihrer Entwicklungsumgebung installieren und damit programmieren.</span><span class="sxs-lookup"><span data-stu-id="33801-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="33801-109">Das Wertversprechen von DWriteCore</span><span class="sxs-lookup"><span data-stu-id="33801-109">The value proposition of DWriteCore</span></span>

<span data-ttu-id="33801-110">[DirectWrite](./direct-write-portal.md) selbst unterstützt ein umfangreiches Array von Features, wodurch es für die meisten Apps unter Windows zum Tool der Wahl beim Rendern von Schriftarten wird, unabhängig davon, ob dies über direkte Aufrufe oder &mdash; [über Direct2D erfolgt.](../direct2d/direct2d-portal.md)</span><span class="sxs-lookup"><span data-stu-id="33801-110">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="33801-111">DirectWrite umfasst ein geräteunabhängiges Textlayoutsystem, qualitativ hochwertiges Microsoft ClearType-Textrendering, hardwarebeschleunigten Text, Mehrformattext® erweiterte [OpenType®](/typography/opentype/) Typografiefeatures, Breitsprachunterstützung und [](/typography/cleartype/) [GDI-kompatibles](../gdi/windows-gdi.md)Layout und Rendering.</span><span class="sxs-lookup"><span data-stu-id="33801-111">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="33801-112">DirectWrite ist seit Windows Vista SP2 verfügbar und hat sich im Laufe der Jahre weiterentwickelt, um erweiterte Features wie variable Schriftarten zu enthalten, die es Entwicklern ermöglichen, Stile, Gewichtungen und andere Attribute auf eine Schriftart mit nur einer Schriftartressource anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="33801-112">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables developers to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="33801-113">Aufgrund der langen Lebensdauer von DirectWrite haben Fortschritte bei der Entwicklung jedoch tendenziell ältere Versionen von Windows zurückgelassen.</span><span class="sxs-lookup"><span data-stu-id="33801-113">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="33801-114">Darüber hinaus ist der Status von DirectWrite als führende Textrenderingtechnologie nur auf Windows beschränkt, wodurch plattformübergreifende Anwendungen entweder ihren eigenen Textrenderingstapel schreiben oder sich auf Lösungen von Drittanbietern verlassen können.</span><span class="sxs-lookup"><span data-stu-id="33801-114">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="33801-115">DWriteCore löst die grundlegenden Probleme des Verwaistens von Versionsfeatures und der plattformübergreifenden Kompatibilität, indem die Bibliothek aus dem System entfernt und alle möglichen unterstützten Endpunkte als Ziel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33801-115">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="33801-116">Zu diesem Zweck haben wir DWriteCore in Project Reunion mit einer öffentlichen API integriert, die auf allen Windows-Endpunkten bis Windows 8 unterstützt wird, und ihnen die Plattformübergreifende Verwendung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="33801-116">To that end, we've integrated DWriteCore into Project Reunion with a public API that's supported on all Windows endpoints down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="33801-117">DWriteCore bietet Ihnen als Entwickler in Project Reunion hauptsächlich den Zugriff auf alle aktuellen DirectWrite-Features bis hin zu Windows 8.</span><span class="sxs-lookup"><span data-stu-id="33801-117">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to all current DirectWrite features all the way down-level to Windows 8.</span></span> <span data-ttu-id="33801-118">Alle Features von DWriteCore funktionieren auf allen Downlevelversionen gleich. Mit anderen Worten: Alle aktuellen Features funktionieren mit Windows 8, Version 8.1 und allen Versionen von Windows 10, ohne dass es zu Ununterschieden in Bezug darauf kommt, welche Features in welchen Versionen funktionieren können.</span><span class="sxs-lookup"><span data-stu-id="33801-118">All features of DWriteCore will function the same on all down-level versions; in other words, all current features will work on Windows 8, 8.1, and all versions of Windows 10, without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="33801-119">Die DWriteCore-Demo-App &mdash; DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="33801-119">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="33801-120">DWriteCore wird anhand der [DWriteCoreGallery-Beispiel-App](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) veranschaulicht, die Sie jetzt herunterladen und untersuchen können.</span><span class="sxs-lookup"><span data-stu-id="33801-120">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="33801-121">Erste Schritte mit DWriteCore</span><span class="sxs-lookup"><span data-stu-id="33801-121">Get started with DWriteCore</span></span>

<span data-ttu-id="33801-122">DWriteCore ist Teil von [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span><span class="sxs-lookup"><span data-stu-id="33801-122">DWriteCore is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="33801-123">In diesem Abschnitt wird beschrieben, wie Sie Ihre Entwicklungsumgebung für die Programmierung mit DWriteCore einrichten.</span><span class="sxs-lookup"><span data-stu-id="33801-123">This section describes how to set up your development environment for programming with DWriteCore.</span></span>

### <a name="install-the-project-reunion-05-vsix"></a><span data-ttu-id="33801-124">Installieren von Project Reunion 0.5 VSIX</span><span class="sxs-lookup"><span data-stu-id="33801-124">Install the Project Reunion 0.5 VSIX</span></span>

<span data-ttu-id="33801-125">Klicken Sie in Visual Studio auf  >  **Erweiterungen Erweiterungen verwalten,** suchen Sie nach *Project Reunion*, und laden Sie die Erweiterung Project Reunion herunter.</span><span class="sxs-lookup"><span data-stu-id="33801-125">In Visual Studio, click **Extensions** > **Manage Extensions**, search for *Project Reunion*, and download the Project Reunion extension.</span></span> <span data-ttu-id="33801-126">Schließen Sie Visual Studio, öffnen Sie sie erneut, und befolgen Sie die Anweisungen, um die Erweiterung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="33801-126">Close and reopen Visual Studio, and follow the prompts to install the extension.</span></span>

<span data-ttu-id="33801-127">Weitere Informationen finden Sie unter [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)und [Erstellen von Desktop-Windows-Apps mit Project Reunion 0.5.](/windows/apps/project-reunion/#set-up-your-development-environment)</span><span class="sxs-lookup"><span data-stu-id="33801-127">For more info, see [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0), and [Build desktop Windows apps with Project Reunion 0.5](/windows/apps/project-reunion/#set-up-your-development-environment).</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="33801-128">Erstellen eines neuen Projekts</span><span class="sxs-lookup"><span data-stu-id="33801-128">Create a new project</span></span>

<span data-ttu-id="33801-129">Erstellen Sie in Visual Studio ein neues Projekt aus der Projektvorlage **Leere App, gepackt (WinUI 3 in Desktop).**</span><span class="sxs-lookup"><span data-stu-id="33801-129">In Visual Studio, create a new project from the **Blank App, Packaged (WinUI 3 in Desktop)** project template.</span></span> <span data-ttu-id="33801-130">Sie finden diese Projektvorlage, indem Sie sprache auswählen: *C++*; platform: *Project Reunion*; Projekttyp: *Desktop*.</span><span class="sxs-lookup"><span data-stu-id="33801-130">You can find that project template by choosing language: *C++*; platform: *Project Reunion*; project type: *Desktop*.</span></span>

<span data-ttu-id="33801-131">Weitere Informationen finden Sie unter [Projektvorlagen für WinUI 3.](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3)</span><span class="sxs-lookup"><span data-stu-id="33801-131">For more info, see [Project templates for WinUI 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).</span></span>

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a><span data-ttu-id="33801-132">Installieren des NuGet-Pakets Microsoft.ProjectReunion.DWrite</span><span class="sxs-lookup"><span data-stu-id="33801-132">Install the Microsoft.ProjectReunion.DWrite NuGet package</span></span>

<span data-ttu-id="33801-133">Klicken Sie in Visual Studio  auf \> **Projekt NuGet-Pakete verwalten...** Durchsuchen , geben Oder fügen Sie \>  **Microsoft.ProjectReunion.DWrite** in das Suchfeld ein, wählen Sie das Element in den Suchergebnissen aus, und klicken Sie dann auf **Installieren,** um das Paket für dieses Projekt zu installieren.</span><span class="sxs-lookup"><span data-stu-id="33801-133">In Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.ProjectReunion.DWrite** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a><span data-ttu-id="33801-134">Alternativ können Sie mit der Beispiel-App DWriteCoreGallery beginnen.</span><span class="sxs-lookup"><span data-stu-id="33801-134">Alternatively, begin with the DWriteCoreGallery sample app</span></span>

<span data-ttu-id="33801-135">Alternativ können Sie mit DWriteCore programmieren, indem Sie mit dem Beispiel-App-Projekt [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) beginnen und Ihre Entwicklung auf diesem Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="33801-135">Alternatively, you can program with DWriteCore by beginning with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span> <span data-ttu-id="33801-136">Anschließend können Sie beliebigen vorhandenen Quellcode (oder dateien) aus diesem Beispielprojekt entfernen und dem Projekt neuen Quellcode (oder neue Dateien) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="33801-136">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span>

### <a name="use-dwritecore-in-your-project"></a><span data-ttu-id="33801-137">Verwenden von DWriteCore in Ihrem Projekt</span><span class="sxs-lookup"><span data-stu-id="33801-137">Use DWriteCore in your project</span></span>

<span data-ttu-id="33801-138">Weitere Informationen zum Programmieren mit DWriteCore finden Sie im Abschnitt Programmieren mit [DWriteCore](#programming-with-dwritecore) weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="33801-138">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="33801-139">Die Releasephasen von DWriteCore</span><span class="sxs-lookup"><span data-stu-id="33801-139">The release phases of DWriteCore</span></span>

<span data-ttu-id="33801-140">Das Portieren von DirectWrite zu DWriteCore ist ein ausreichend großes Projekt, das mehrere Windows-Releasezyklen umfassen kann.</span><span class="sxs-lookup"><span data-stu-id="33801-140">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="33801-141">Dieses Projekt ist in Phasen unterteilt, die jeweils einem Teil der In einem Release bereitgestellten Funktionalität entsprechen.</span><span class="sxs-lookup"><span data-stu-id="33801-141">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="33801-142">Features in der aktuellen Version von DWriteCore</span><span class="sxs-lookup"><span data-stu-id="33801-142">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="33801-143">Die derzeit verfügbare Version von DWriteCore enthält die grundlegenden Tools, die Sie als Entwickler benötigen, um DWriteCore zu nutzen, einschließlich der folgenden Features.</span><span class="sxs-lookup"><span data-stu-id="33801-143">The version of DWriteCore currently available contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="33801-144">Schriftartenenumeration.</span><span class="sxs-lookup"><span data-stu-id="33801-144">Font enumeration.</span></span>
- <span data-ttu-id="33801-145">Schriftart-API.</span><span class="sxs-lookup"><span data-stu-id="33801-145">Font API.</span></span>
- <span data-ttu-id="33801-146">Gestaltung.</span><span class="sxs-lookup"><span data-stu-id="33801-146">Shaping.</span></span>
- <span data-ttu-id="33801-147">Rendering-APIs auf niedriger Ebene.</span><span class="sxs-lookup"><span data-stu-id="33801-147">Low-level rendering APIs.</span></span> <span data-ttu-id="33801-148">Dies ist teilweise in der aktuellen Phase DWriteCore funktioniert nicht mit &mdash; [Direct2D,](../direct2d/direct2d-portal.md)aber Sie können [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) und [**IDWriteBitmapRenderTarget verwenden.**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)</span><span class="sxs-lookup"><span data-stu-id="33801-148">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="33801-149">Grundlegende Textlayoutfunktionalität.</span><span class="sxs-lookup"><span data-stu-id="33801-149">Basic text layout functionality.</span></span>
- <span data-ttu-id="33801-150">Textrendering-APIs.</span><span class="sxs-lookup"><span data-stu-id="33801-150">Text-rendering APIs.</span></span>
- <span data-ttu-id="33801-151">Bitmaprenderingziel.</span><span class="sxs-lookup"><span data-stu-id="33801-151">Bitmap render target.</span></span>
- <span data-ttu-id="33801-152">Farbschriftarten.</span><span class="sxs-lookup"><span data-stu-id="33801-152">Color fonts.</span></span>
- <span data-ttu-id="33801-153">Verschiedene Optimierungen (Bereinigung des Schriftartcaches, In-Memory-Schriftartlademodul und so weiter).</span><span class="sxs-lookup"><span data-stu-id="33801-153">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="33801-154">Das Bannerfeature in dieser Phase ist Farbschriftarten.</span><span class="sxs-lookup"><span data-stu-id="33801-154">The banner feature at this stage is color fonts.</span></span> <span data-ttu-id="33801-155">MitHilfe von Farbschriftarten können Sie Ihre Schriftarten mit komplexeren Farbfunktionen rendern, die über einfache Einzelfarben hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="33801-155">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="33801-156">Farbschriftarten sind z. B. die Möglichkeit, Emoji- und Symbolsymbolschriftarten zu rendern (letzteres wird z. B. von Office verwendet).</span><span class="sxs-lookup"><span data-stu-id="33801-156">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="33801-157">Farbschriftarten wurden erstmals in Windows 8.1 eingeführt, aber das Feature wurde in Windows 10 Version 1607 (Anniversary Update) stark erweitert.</span><span class="sxs-lookup"><span data-stu-id="33801-157">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="33801-158">Die Arbeit an der Bereinigung des Schriftartcaches und des In-Memory-Schriftartlademoduls ermöglicht ein schnelleres Laden von Schriftarten und Speicherverbesserungen.</span><span class="sxs-lookup"><span data-stu-id="33801-158">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="33801-159">Mit diesen Features können Sie sofort damit beginnen, einige der modernen Kernfunktionen von DirectWrite zu nutzen, z. B. &mdash; variable Schriftarten &mdash; auf Windows 8.</span><span class="sxs-lookup"><span data-stu-id="33801-159">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts&mdash;down-level to Windows 8.</span></span> <span data-ttu-id="33801-160">Diese Iteration der Bibliothek kann auch unter [Android](https://www.android.com/)und **Linux** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33801-160">This iteration of the library can also be consumed on [Android](https://www.android.com/), and **Linux**.</span></span> <span data-ttu-id="33801-161">Variable Schriftarten sind eines der wichtigsten Features für DirectWrite-Kunden. sie wurden in Windows 10 Version 1709 (Fall Creators Update) eingeführt, sodass der Zugriff auf sie in früheren Versionen ein großer Boon für Sie als Entwickler ist.</span><span class="sxs-lookup"><span data-stu-id="33801-161">Variable fonts are one of the most important features for DirectWrite customers; they were introduced in Windows 10, version 1709 (Fall Creators Update), so accessing them in previous versions is a massive boon to you as a developer.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="33801-162">Unsere Einladung für Sie als DirectWrite-Entwickler</span><span class="sxs-lookup"><span data-stu-id="33801-162">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="33801-163">DWriteCore wird zusammen mit anderen Project Reunion-Komponenten mit Entwicklerfeedback entwickelt.</span><span class="sxs-lookup"><span data-stu-id="33801-163">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="33801-164">Wir laden Sie ein, mit dem Erkunden von DWriteCore zu beginnen und Einblicke oder Anforderungen in die Featureentwicklung in unserem [GitHub-Repository Project Reunion](https://github.com/microsoft/ProjectReunion/)bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="33801-164">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="33801-165">Programmieren mit DWriteCore</span><span class="sxs-lookup"><span data-stu-id="33801-165">Programming with DWriteCore</span></span>

<span data-ttu-id="33801-166">Genau wie bei [DirectWrite programmieren](./direct-write-portal.md)Sie mit DWriteCore über die COM-Light-API über die [**IDWriteFactory-Schnittstelle.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)</span><span class="sxs-lookup"><span data-stu-id="33801-166">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="33801-167">Um DWriteCore zu verwenden, muss die Headerdatei eingeschlossen `dwrite_core.h` werden.</span><span class="sxs-lookup"><span data-stu-id="33801-167">To use DWriteCore, it's necessary to include the `dwrite_core.h` header file.</span></span>

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

<span data-ttu-id="33801-168">Die `dwrite_core.h` Headerdatei definiert zuerst das Token *DWRITE_CORE* und enthält dann `dwrite_3.h` .</span><span class="sxs-lookup"><span data-stu-id="33801-168">The `dwrite_core.h` header file first defines the token *DWRITE_CORE*, and then it includes `dwrite_3.h`.</span></span> <span data-ttu-id="33801-169">Das *DWRITE_CORE* Token ist wichtig, da es alle nachfolgend enthaltenen Header anleitet, ihnen alle DirectWrite-APIs zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="33801-169">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="33801-170">Sobald Ihr Projekt enthalten `dwrite_core.h` ist, können Sie Code schreiben, erstellen und ausführen.</span><span class="sxs-lookup"><span data-stu-id="33801-170">Once your project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="33801-171">APIs, die für DWriteCore neu oder anders sind</span><span class="sxs-lookup"><span data-stu-id="33801-171">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="33801-172">Die DWriteCore-API-Oberfläche ist größtenteils identisch mit der für [DirectWrite.](/windows/win32/api/_directwrite/)</span><span class="sxs-lookup"><span data-stu-id="33801-172">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="33801-173">Es gibt jedoch eine kleine Anzahl neuer APIs, die derzeit nur in DWriteCore vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="33801-173">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="33801-174">Erstellen eines eingeschränkten Factoryobjekts</span><span class="sxs-lookup"><span data-stu-id="33801-174">Create a restricted factory object</span></span>

<span data-ttu-id="33801-175">Die [**DWRITE_FACTORY_TYPE-Enumeration**](./dwrite/ne-dwrite-dwrite_factory_type.md) verfügt über eine neue Konstante &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, die eine eingeschränkte Factory angibt.</span><span class="sxs-lookup"><span data-stu-id="33801-175">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_ISOLATED2**, indicating a restricted factory.</span></span> <span data-ttu-id="33801-176">Eine eingeschränkte Factory ist stärker gesperrt als eine isolierte Factory.</span><span class="sxs-lookup"><span data-stu-id="33801-176">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="33801-177">Es interagiert in irgendeiner Weise nicht mit einem prozessübergreifenden oder beständigen Schriftartcache.</span><span class="sxs-lookup"><span data-stu-id="33801-177">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="33801-178">Darüber hinaus enthält die von dieser Factory zurückgegebene Auflistung von Systemschriftarten nur bekannte Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="33801-178">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="33801-179">So können Sie mithilfe von **DWRITE_FACTORY_TYPE_ISOLATED2** ein eingeschränktes Factoryobjekt erstellen, wenn Sie die freie [**DWriteCoreCreateFactory-Funktion**](/windows/win32/api/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="33801-179">Here's how you can use **DWRITE_FACTORY_TYPE_ISOLATED2** to create a restricted factory object when you call the [**DWriteCoreCreateFactory**](/windows/win32/api/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) free function.</span></span>

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

<span data-ttu-id="33801-180">Wenn Sie **DWRITE_FACTORY_TYPE_ISOLATED2** an eine ältere Version von DirectWrite übergeben, die sie nicht unterstützt, gibt **DWriteCreateFactory** **E_INVALIDARG.**</span><span class="sxs-lookup"><span data-stu-id="33801-180">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="33801-181">Zeichnen von Glyphen in eine Systemspeicherbitmap</span><span class="sxs-lookup"><span data-stu-id="33801-181">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="33801-182">DirectWrite verfügt über eine Bitmap-Renderzielschnittstelle, die das Rendern von Glyphen in eine Bitmap im Systemspeicher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33801-182">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="33801-183">Derzeit besteht die einzige Möglichkeit, zugriff auf die zugrunde liegenden Pixeldaten zu erhalten, in der Verwendung von GDI, sodass die API nicht plattformübergreifend verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="33801-183">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="33801-184">Dies lässt sich leicht beheben, indem eine Methode zum Abrufen der Pixeldaten hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="33801-184">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="33801-185">DWriteCore führt daher die [**IDWriteBitmapRenderTarget2-Schnittstelle**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) und deren [**Methode IDWriteBitmapRenderTarget2::GetBitmapData ein.**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md)</span><span class="sxs-lookup"><span data-stu-id="33801-185">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="33801-186">Diese Methode akzeptiert einen Parameter des Typs (Zeiger auf) DWRITE_BITMAP_DATA_BGRA32 [**,**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md)bei dem es sich um eine neue Struktur handelt.</span><span class="sxs-lookup"><span data-stu-id="33801-186">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="33801-187">Ihre Anwendung erstellt ein Bitmaprenderingziel durch Aufrufen von [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="33801-187">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="33801-188">Unter Windows kapselt ein Bitmaprenderingziel einen GDI-Speicherdomänencontroller mit einer GDI-DIB(Device-Independent Bitmap), die ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="33801-188">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="33801-189">[IDWriteBitmapRenderTarget::D rawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) rendert Glyphen im DIB.</span><span class="sxs-lookup"><span data-stu-id="33801-189">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="33801-190">DirectWrite rendert die Glyphen selbst, ohne GDI zu durchschreiten.</span><span class="sxs-lookup"><span data-stu-id="33801-190">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="33801-191">Ihre Anwendung kann dann den **HDC** aus dem Bitmaprenderingziel abrufen und [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) verwenden, um die Pixel in ein **HDC-Fenster** zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="33801-191">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="33801-192">Auf Nicht-Windows-Plattformen kann Ihre Anwendung weiterhin ein Bitmaprenderingziel erstellen, kapselt aber einfach ein Systemspeicherarray ohne **HDC** und ohne DIB.</span><span class="sxs-lookup"><span data-stu-id="33801-192">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="33801-193">Ohne **HDC** muss es eine andere Möglichkeit für Ihre Anwendung geben, die Bitmappixel abzurufen, damit sie sie kopieren oder anderweitig verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="33801-193">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="33801-194">Selbst unter Windows ist es manchmal nützlich, die tatsächlichen Pixeldaten abzurufen, und wir zeigen die aktuelle Vorgehensweise im folgenden Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="33801-194">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="33801-195">Andere API-Unterschiede zwischen DWriteCore und DirectWrite</span><span class="sxs-lookup"><span data-stu-id="33801-195">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="33801-196">Es gibt einige APIs, die entweder nur Stubs sind oder sich auf Nicht-Windows-Plattformen etwas anders verhalten.</span><span class="sxs-lookup"><span data-stu-id="33801-196">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="33801-197">Beispielsweise gibt [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) **E_NOTIMPL** auf Nicht-Windows-Plattformen zurück, da es kein **HDC** ohne [GDI](../gdi/windows-gdi.md)gibt.</span><span class="sxs-lookup"><span data-stu-id="33801-197">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="33801-198">Und schließlich gibt es bestimmte andere Windows-APIs, die in der Regel zusammen mit DirectWrite verwendet werden (Direct2D ist ein bedeutendes Beispiel).</span><span class="sxs-lookup"><span data-stu-id="33801-198">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="33801-199">Derzeit können Direct2D und DWriteCore jedoch nicht zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="33801-199">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="33801-200">Wenn Sie beispielsweise ein [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mit DWriteCore erstellen und es an [**D2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)übergeben, tritt bei diesem Aufruf ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="33801-200">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>
