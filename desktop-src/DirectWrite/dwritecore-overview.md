---
title: Übersicht über DWriteCore
description: Dschreitecore ist die Projekt-Reunion-Implementierung von DirectWrite.
keywords:
- DirectWrite-Kern
- DWriteCore
ms.topic: article
ms.date: 12/09/2020
ms.openlocfilehash: 605cab8d0cd0511b5ca3b0b14d517cdc3f290573
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351038"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="0830c-105">Übersicht über DWriteCore</span><span class="sxs-lookup"><span data-stu-id="0830c-105">DWriteCore overview</span></span>

<span data-ttu-id="0830c-106">Dschreitecore ist die [Projekt-Reunion](/windows/apps/project-reunion/) -Implementierung von [DirectWrite](./direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="0830c-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md).</span></span> <span data-ttu-id="0830c-107">DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="0830c-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="0830c-108">In diesem Einführungs Thema wird beschrieben, was dscriptecore ist, und es wird gezeigt, wie Sie es in der Entwicklungsumgebung installieren und mit ihm programmieren.</span><span class="sxs-lookup"><span data-stu-id="0830c-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="0830c-109">Der Wertbeitrag von dschreitecore.</span><span class="sxs-lookup"><span data-stu-id="0830c-109">The value proposition of DWriteCore</span></span>

<span data-ttu-id="0830c-110">[DirectWrite](./direct-write-portal.md) selbst unterstützt eine umfangreiche Palette von Features, die es als Tool zur Schriftart Rendering in Windows für die meisten apps bereitstellt, unabhängig davon &mdash; , ob dies durch direkte Aufrufe oder über [Direct2D](../direct2d/direct2d-portal.md)erfolgt.</span><span class="sxs-lookup"><span data-stu-id="0830c-110">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="0830c-111">DirectWrite enthält ein Geräte unabhängiges textlayoutsystem, hochwertige Subpixel-Text Rendering von [Microsoft ClearType](/typography/cleartype/) , Hardware beschleunigter Text, mehrstufiger Text, erweiterter [OpenType-®](/typography/opentype/) Typografiefeatures, breiten Sprachunterstützung und [GDI](../gdi/windows-gdi.md)-kompatibles Layout und Rendering.</span><span class="sxs-lookup"><span data-stu-id="0830c-111">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="0830c-112">DirectWrite ist seit Windows Vista SP2 verfügbar und wurde im Laufe der Jahre erweitert, um erweiterte Features wie z. b. Variablen Schriftarten zu enthalten, mit denen Entwickler Stile, Gewichtungen und andere Attribute auf eine Schriftart mit nur einer Schriftart Ressource anwenden können.</span><span class="sxs-lookup"><span data-stu-id="0830c-112">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables developers to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="0830c-113">Aufgrund der langen Lebensdauer von DirectWrite haben Entwicklungsfortschritte tendenziell ältere Versionen von Windows hinter sich gelassen.</span><span class="sxs-lookup"><span data-stu-id="0830c-113">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="0830c-114">Außerdem ist der Status von DirectWrite als Premier-textrenderingtechnologie nur auf Windows beschränkt, sodass plattformübergreifende Anwendungen entweder ihren eigenen Text Rendering-Stapel schreiben oder auf Drittanbieter Lösungen basieren können.</span><span class="sxs-lookup"><span data-stu-id="0830c-114">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="0830c-115">Dbeschreib tecore löst die grundlegenden Probleme des verwaisen-und plattformübergreifenden Kompatibilitäts Problems, indem die Bibliothek aus dem System entfernt und alle möglichen unterstützten Endpunkte als Ziel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0830c-115">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="0830c-116">Zu diesem Zweck haben wir dwrite-Core in Project Reunion mit einer öffentlichen API integriert, die von allen Windows-Endpunkten bis zu Windows 8 unterstützt wird. Sie öffnet die Tür, in der Sie Sie plattformübergreifend verwenden können.</span><span class="sxs-lookup"><span data-stu-id="0830c-116">To that end, we've integrated DWriteCore into Project Reunion with a public API that's supported on all Windows endpoints down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="0830c-117">Der primäre Wert, den dwrite-Core Ihnen als Entwickler in Project Reunion bietet, besteht darin, dass er den Zugriff auf alle aktuellen DirectWrite-Features auf die gleiche Weise wie auf Windows 8 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="0830c-117">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to all current DirectWrite features all the way down-level to Windows 8.</span></span> <span data-ttu-id="0830c-118">Alle Features von dbeschreib tecore funktionieren in allen Versionen mit untergeordneten Versionen identisch. mit anderen Worten: alle aktuellen Features funktionieren unter Windows 8, 8,1 und allen Versionen von Windows 10, ohne dass Unterschiede in Bezug auf die Funktionsweise der Versionen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="0830c-118">All features of DWriteCore will function the same on all down-level versions; in other words, all current features will work on Windows 8, 8.1, and all versions of Windows 10, without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="0830c-119">Die dwrite-Core-Demo-App &mdash; dschreitecoregallery</span><span class="sxs-lookup"><span data-stu-id="0830c-119">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="0830c-120">Dwrite-Core wird anhand der Beispiel-APP [dschreitecoregallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) veranschaulicht, die Sie jetzt herunterladen und untersuchen können.</span><span class="sxs-lookup"><span data-stu-id="0830c-120">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="0830c-121">Einstieg in dwrite-Core</span><span class="sxs-lookup"><span data-stu-id="0830c-121">Get started with DWriteCore</span></span>

<span data-ttu-id="0830c-122">Bei der Vorabversion von Project Reunion 0,1 wird die Installation des nuget-Pakets Project Reunion in ihren eigenen Projekten derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0830c-122">For the Project Reunion 0.1 Prerelease, we currently don't support installing the Project Reunion NuGet package into your own projects.</span></span> <span data-ttu-id="0830c-123">Die derzeit unterstützte Option für Ihre eigene Programmierung mit dwrite-Core besteht darin, mit dem Projekt " [dwrite tecoregallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) -Beispiel-app" zu beginnen und ihre Entwicklung auf diesem Projekt zu basieren.</span><span class="sxs-lookup"><span data-stu-id="0830c-123">Instead, the currently supported option for your own programming with DWriteCore is to begin with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span>

<span data-ttu-id="0830c-124">Anschließend können Sie den vorhandenen Quellcode (oder Dateien) aus dem Beispiel Projekt entfernen und dem Projekt jeden neuen Quellcode (oder Dateien) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0830c-124">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span> <span data-ttu-id="0830c-125">Weitere Informationen zum Programmieren mit dwrite Core finden Sie im Abschnitt [Programmieren mit dbeschreib tecore](#programming-with-dwritecore) weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="0830c-125">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="0830c-126">Die releasephasen von dbeschreib tecore</span><span class="sxs-lookup"><span data-stu-id="0830c-126">The release phases of DWriteCore</span></span>

<span data-ttu-id="0830c-127">Das Portieren von DirectWrite auf dbeschreib tecore ist ein ausreichend großes Projekt, das mehrere Windows-Releasezyklen umfasst.</span><span class="sxs-lookup"><span data-stu-id="0830c-127">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="0830c-128">Dieses Projekt ist in Phasen unterteilt, von denen jede einem Funktionsblock entspricht, der in einem Release geliefert wird.</span><span class="sxs-lookup"><span data-stu-id="0830c-128">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="0830c-129">Funktionen in der aktuellen Version von dbeschreib tecore</span><span class="sxs-lookup"><span data-stu-id="0830c-129">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="0830c-130">Die derzeit verfügbare Version von dbeschreib tecore enthält die grundlegenden Tools, die Sie als Entwickler für dwrite verwenden müssen, einschließlich der folgenden Features.</span><span class="sxs-lookup"><span data-stu-id="0830c-130">The version of DWriteCore currently available contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="0830c-131">Font-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="0830c-131">Font enumeration.</span></span>
- <span data-ttu-id="0830c-132">Schriftart-API.</span><span class="sxs-lookup"><span data-stu-id="0830c-132">Font API.</span></span>
- <span data-ttu-id="0830c-133">Mit.</span><span class="sxs-lookup"><span data-stu-id="0830c-133">Shaping.</span></span>
- <span data-ttu-id="0830c-134">Rendering-APIs auf niedriger Ebene.</span><span class="sxs-lookup"><span data-stu-id="0830c-134">Low-level rendering APIs.</span></span> <span data-ttu-id="0830c-135">Dies ist in der aktuellen Phase partiell &mdash; . dbeschreib tecore interagiert nicht mit [Direct2D](../direct2d/direct2d-portal.md), Sie können jedoch [**idschreiteglyphrunanalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) und [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)verwenden.</span><span class="sxs-lookup"><span data-stu-id="0830c-135">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="0830c-136">Grundlegende textlayoutfunktionen.</span><span class="sxs-lookup"><span data-stu-id="0830c-136">Basic text layout functionality.</span></span>
- <span data-ttu-id="0830c-137">Text Rendering-APIs.</span><span class="sxs-lookup"><span data-stu-id="0830c-137">Text-rendering APIs.</span></span>
- <span data-ttu-id="0830c-138">Das Renderziel der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="0830c-138">Bitmap render target.</span></span>
- <span data-ttu-id="0830c-139">Farb Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="0830c-139">Color fonts.</span></span>
- <span data-ttu-id="0830c-140">Sonstige Optimierungen (Schriftart Cache Bereinigung, in-Memory-Schriftart Lade Tool usw.).</span><span class="sxs-lookup"><span data-stu-id="0830c-140">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="0830c-141">Die Banner Funktion in dieser Phase ist Farb Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="0830c-141">The banner feature at this stage is color fonts.</span></span> <span data-ttu-id="0830c-142">Mit Farb Schriftarten können Sie Ihre Schriftarten mit einer komplexeren Farb Funktionalität über einfache einzelne Farben hinaus Rendering.</span><span class="sxs-lookup"><span data-stu-id="0830c-142">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="0830c-143">Mit Color Fonts können z. b. emoji und Symbol Schriftarten von Symbolleisten dargestellt werden (die letztere wird beispielsweise von Office verwendet).</span><span class="sxs-lookup"><span data-stu-id="0830c-143">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="0830c-144">Farb Schriftarten wurden erstmals in Windows 8.1 eingeführt, aber das Feature wurde in Windows 10, Version 1607 (Anniversary Update), stark erweitert.</span><span class="sxs-lookup"><span data-stu-id="0830c-144">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="0830c-145">Mit der Bereinigung des Schriftart Caches und dem in-Memory-Schriftart Lade Tool können Sie ein schnelleres Laden von Schriftarten und Arbeitsspeicher Verbesserungen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0830c-145">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="0830c-146">Mit diesen Features können Sie sofort mit der Nutzung einiger der modernen Kernfunktionen von DirectWrite, &mdash; wie z. b. variabler Schriftarten &mdash; auf Windows 8, beginnen.</span><span class="sxs-lookup"><span data-stu-id="0830c-146">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts&mdash;down-level to Windows 8.</span></span> <span data-ttu-id="0830c-147">Diese Iterationen der Bibliothek können auch unter [Android](https://www.android.com/)und **Linux** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0830c-147">This iteration of the library can also be consumed on [Android](https://www.android.com/), and **Linux**.</span></span> <span data-ttu-id="0830c-148">Variablen Schriftarten sind eines der wichtigsten Features für DirectWrite-Kunden. Sie wurden in Windows 10, Version 1709 (Fall Creators Update), eingeführt, sodass der Zugriff in früheren Versionen ein großer Segen für Sie als Entwickler ist.</span><span class="sxs-lookup"><span data-stu-id="0830c-148">Variable fonts are one of the most important features for DirectWrite customers; they were introduced in Windows 10, version 1709 (Fall Creators Update), so accessing them in previous versions is a massive boon to you as a developer.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="0830c-149">Unsere Einladung als DirectWrite-Entwickler</span><span class="sxs-lookup"><span data-stu-id="0830c-149">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="0830c-150">Dbeschreib tecore wird zusammen mit anderen Project Reunion-Komponenten mit Offenheit für Entwickler Feedback entwickelt.</span><span class="sxs-lookup"><span data-stu-id="0830c-150">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="0830c-151">Wir laden Sie ein, mit der Untersuchung von dwrite-Core zu beginnen und Einblicke oder Anforderungen für die Featureentwicklung in unserem [GitHub-Repository Project Reunion](https://github.com/microsoft/ProjectReunion/)bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0830c-151">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="0830c-152">Programmieren mit dschreitecore</span><span class="sxs-lookup"><span data-stu-id="0830c-152">Programming with DWriteCore</span></span>

<span data-ttu-id="0830c-153">Wie bereits erwähnt, ist für die Vorabversion von Project Reunion 0,1 die derzeit unterstützte Option für Ihre eigene Programmierung mit dwrite-Core, mit dem Projekt " [dwrite tecoregallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) "-Beispiel-APP zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="0830c-153">As already mentioned, for the Project Reunion 0.1 Prerelease, the currently supported option for your own programming with DWriteCore is to begin with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project.</span></span>

<span data-ttu-id="0830c-154">Ebenso wie bei [DirectWrite](./direct-write-portal.md)programmieren Sie mithilfe der com-Light-API über die [**idbeschreib tefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Schnittstelle mit dwrite-Core.</span><span class="sxs-lookup"><span data-stu-id="0830c-154">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="0830c-155">**Dschreitecoregallery** enthält bereits die `dwrite_core.h` Header Datei.</span><span class="sxs-lookup"><span data-stu-id="0830c-155">**DWriteCoreGallery** already includes the `dwrite_core.h` header file.</span></span> <span data-ttu-id="0830c-156">Dieser Header definiert zuerst das Token *DWRITE_CORE* und schließt dann ein `dwrite_3.h` .</span><span class="sxs-lookup"><span data-stu-id="0830c-156">That header first defines the token *DWRITE_CORE*, and then it includes `dwrite_3.h`.</span></span> <span data-ttu-id="0830c-157">Das *DWRITE_CORE* Token ist wichtig, da es alle später enthaltenen Header anweist, alle DirectWrite-APIs für Sie verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="0830c-157">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="0830c-158">Sobald ein Projekt enthalten ist `dwrite_core.h` , können Sie Code schreiben, erstellen und ausführen.</span><span class="sxs-lookup"><span data-stu-id="0830c-158">Once a project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

```cppwinrt
// pch.h
...
#include <dwrite_core.h>
```

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="0830c-159">Neue oder andere APIs für dwrite Core</span><span class="sxs-lookup"><span data-stu-id="0830c-159">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="0830c-160">Die API-Oberfläche für die dschreitecore-API ist größtenteils identisch mit der für [DirectWrite](/windows/win32/api/_directwrite/).</span><span class="sxs-lookup"><span data-stu-id="0830c-160">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="0830c-161">Es gibt jedoch eine kleine Anzahl von neuen APIs, die derzeit nur in dwrite-Core vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="0830c-161">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="0830c-162">Erstellen eines eingeschränkten Factory-Objekts</span><span class="sxs-lookup"><span data-stu-id="0830c-162">Create a restricted factory object</span></span>

<span data-ttu-id="0830c-163">Die [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) -Enumeration verfügt über eine neue Konstante &mdash; **DWRITE_FACTORY_TYPE_RESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="0830c-163">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_RESTRICTED**.</span></span> <span data-ttu-id="0830c-164">Eine eingeschränkte Factory ist besser gesperrt als eine isolierte Factory.</span><span class="sxs-lookup"><span data-stu-id="0830c-164">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="0830c-165">Es findet in keiner Weise eine Interaktion mit einem prozessübergreifenden oder permanenten Schriftart Cache.</span><span class="sxs-lookup"><span data-stu-id="0830c-165">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="0830c-166">Außerdem enthält die von dieser Factory zurückgegebene System Schriftart Auflistung nur bekannte Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="0830c-166">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="0830c-167">Im folgenden wird erläutert, wie Sie **DWRITE_FACTORY_TYPE_RESTRICTED** ein eingeschränktes Factory-Objekt erstellen können, wenn Sie die Free-Funktion von [**dwrite Items | atefactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0830c-167">Here's how you can use **DWRITE_FACTORY_TYPE_RESTRICTED** to create a restricted factory object when you call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) free function.</span></span>

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCreateFactory(
    DWRITE_FACTORY_TYPE_RESTRICTED,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

<span data-ttu-id="0830c-168">Wenn Sie **DWRITE_FACTORY_TYPE_RESTRICTED** an eine ältere Version von DirectWrite übergeben, die dies nicht unterstützt, gibt **dschreitekreatefactory** **E_INVALIDARG** zurück.</span><span class="sxs-lookup"><span data-stu-id="0830c-168">If you pass **DWRITE_FACTORY_TYPE_RESTRICTED** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="0830c-169">Zeichnen von Glyphen in eine Bitmap des System Speichers</span><span class="sxs-lookup"><span data-stu-id="0830c-169">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="0830c-170">DirectWrite verfügt über eine Bitmap-Renderziel-Schnittstelle, die das Rendern von Glyphen in eine Bitmap im Systemspeicher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0830c-170">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="0830c-171">Die einzige Möglichkeit, auf die zugrunde liegenden Pixeldaten zuzugreifen, besteht jedoch darin, GDI zu durchlaufen, sodass die API nicht plattformübergreifend verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0830c-171">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="0830c-172">Dies kann problemlos durch Hinzufügen einer Methode zum Abrufen der Pixeldaten behoben werden.</span><span class="sxs-lookup"><span data-stu-id="0830c-172">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="0830c-173">Daher führt dwrite tecore die [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) -Schnittstelle und die zugehörige-Methode [**IDWriteBitmapRenderTarget2:: getbitmapdata**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md)ein.</span><span class="sxs-lookup"><span data-stu-id="0830c-173">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="0830c-174">Diese Methode nimmt einen Parameter vom Typ (Zeiger auf) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md)auf, bei dem es sich um eine neue Struktur handelt.</span><span class="sxs-lookup"><span data-stu-id="0830c-174">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="0830c-175">Die Anwendung erstellt ein Bitmap-Renderziel durch Aufrufen von [idwrite tegdiinterop:: createbitmaprendertarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="0830c-175">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="0830c-176">Unter Windows kapselt ein Bitmap-Renderziel einen GDI-Speicher-DC mit einem ausgewählten GDI-geräteunabhängigen Bitmap (DIB).</span><span class="sxs-lookup"><span data-stu-id="0830c-176">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="0830c-177">[Idschreitebitmaprendertarget::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) rendert Symbole zum DIB.</span><span class="sxs-lookup"><span data-stu-id="0830c-177">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="0830c-178">DirectWrite rendert die Symbole selbst, ohne dass GDI durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="0830c-178">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="0830c-179">Die Anwendung kann dann den **hdc** aus dem Bitmap-Renderziel erhalten und mit [BitBLT](/windows/win32/api/wingdi/nf-wingdi-bitblt) die Pixel in ein Windows- **hdc** kopieren.</span><span class="sxs-lookup"><span data-stu-id="0830c-179">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="0830c-180">Auf nicht-Windows-Plattformen kann die Anwendung immer noch ein Bitmap-Renderziel erstellen, aber Sie kapselt lediglich ein Systemspeicher Array ohne **hdc** und kein DIB.</span><span class="sxs-lookup"><span data-stu-id="0830c-180">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="0830c-181">Ohne einen **hdc** muss Ihre Anwendung eine andere Möglichkeit aufweisen, um die Bitmap-Pixel zu erhalten, damit Sie Sie kopieren oder anderweitig verwenden können.</span><span class="sxs-lookup"><span data-stu-id="0830c-181">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="0830c-182">Auch unter Windows ist es manchmal sinnvoll, die eigentlichen Pixeldaten zu erhalten. im folgenden Codebeispiel wird die aktuelle Methode gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0830c-182">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="0830c-183">Weitere API-Unterschiede zwischen dwrite-Core und DirectWrite</span><span class="sxs-lookup"><span data-stu-id="0830c-183">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="0830c-184">Es gibt ein paar APIs, bei denen es sich entweder um Stubel handelt oder die sich auf nicht-Windows-Plattformen anders Verhalten.</span><span class="sxs-lookup"><span data-stu-id="0830c-184">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="0830c-185">Beispielsweise gibt [idwrite tegdiinterop:: anatefontfakefromhdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) **E_NOTIMPL** auf nicht-Windows-Plattformen zurück, da es keinen **hdc** ohne [GDI](../gdi/windows-gdi.md)gibt.</span><span class="sxs-lookup"><span data-stu-id="0830c-185">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="0830c-186">Und schließlich gibt es bestimmte andere Windows-APIs, die normalerweise in Verbindung mit DirectWrite verwendet werden (Direct2D ist ein wichtiges Beispiel).</span><span class="sxs-lookup"><span data-stu-id="0830c-186">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="0830c-187">Allerdings funktionieren Direct2D und dwrite tecore derzeit nicht.</span><span class="sxs-lookup"><span data-stu-id="0830c-187">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="0830c-188">Wenn Sie z. b. ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mithilfe von dwrite-Core erstellen und es an [**D2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)übergeben, schlägt dieser Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="0830c-188">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>