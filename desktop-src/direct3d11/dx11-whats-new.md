---
title: Neuerungen im SDK für Windows 7/Direct3D 11 vom August 2009
description: Diese Version von Windows 7/Direct3D 11 wird als Teil des DirectX SDK ausgeliefert und enthält neue Features, Tools und Dokumentationen.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5e600e5dff679129bb9d007b9f1659bfd018d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103731560"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a><span data-ttu-id="cf950-103">Neuerungen im SDK für Windows 7/Direct3D 11 vom August 2009</span><span class="sxs-lookup"><span data-stu-id="cf950-103">What's New in the August 2009 Windows 7/Direct3D 11 SDK</span></span>

<span data-ttu-id="cf950-104">Diese Version von Windows 7/Direct3D 11 wird als Teil des DirectX SDK ausgeliefert und enthält neue Features, Tools und Dokumentationen.</span><span class="sxs-lookup"><span data-stu-id="cf950-104">This version of Windows 7/Direct3D 11 ships as part of the DirectX SDK and contains new features, tools, and documentation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf950-105">Element</span><span class="sxs-lookup"><span data-stu-id="cf950-105">Item</span></span></th>
<th><span data-ttu-id="cf950-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf950-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf950-107"><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D</span><span class="sxs-lookup"><span data-stu-id="cf950-107"><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D</span></span><br/></td>
<td><span data-ttu-id="cf950-108">Bei Direct2D handelt es sich um eine hardwarebeschleunigte, 2D-Grafik-API, die leistungsstarke und qualitativ hochwertige Rendering für 2-d-Geometrie, Bitmaps und Text bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cf950-108">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="cf950-109">Die Direct2D-API ist für die Zusammenarbeit mit Direct3D und GDI konzipiert.</span><span class="sxs-lookup"><span data-stu-id="cf950-109">The Direct2D API is designed to interoperate well with Direct3D and GDI.</span></span> <span data-ttu-id="cf950-110">Mit diesem SDK können Entwickler die API auswerten und einfache Anwendungen schreiben, mit einigen der erweiterten Funktionen, die auf ordnungsgemäß konfigurierten Computern möglich sind.</span><span class="sxs-lookup"><span data-stu-id="cf950-110">This SDK allows developers to evaluate the API and write simple applications, with some of the more advanced functionality possible on properly configured machines.</span></span> <br/> <span data-ttu-id="cf950-111"><a href="/windows/win32/direct2d/direct2d-portal">Dokumentation</a> und <a href="/previous-versions//dd372354(v=vs.85)">Beispiele</a> für Direct2D sind zurzeit auf MSDN verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cf950-111"><a href="/windows/win32/direct2d/direct2d-portal">Documentation</a> and <a href="/previous-versions//dd372354(v=vs.85)">samples</a> for Direct2D are currently available on MSDN.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf950-112"><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite</span><span class="sxs-lookup"><span data-stu-id="cf950-112"><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite</span></span><br/></td>
<td><span data-ttu-id="cf950-113">DirectWrite bietet Unterstützung für hochwertige Text Rendering, auflösungsunabhängige Gliederungs Schriftarten, vollständige Unicode-Text-und Layoutunterstützung und vieles mehr:</span><span class="sxs-lookup"><span data-stu-id="cf950-113">DirectWrite provides support for high-quality text rendering, resolution-independent outline fonts, full Unicode text and layout support, and much, much more:</span></span><br/>
<ul>
<li><span data-ttu-id="cf950-114">Ein Geräte unabhängiges textlayoutsystem zur Verbesserung der Lesbarkeit von Text in Dokumenten und in der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="cf950-114">A device-independent text layout system that improves text readability in documents and in UI.</span></span><br/></li>
<li><span data-ttu-id="cf950-115">Hochwertiges, unter Pixel-, ClearType-Text Rendering, das GDI-Direct3D, Direct2D oder anwendungsspezifische renderingtechnologie verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="cf950-115">High-quality, sub-pixel, ClearType text rendering that can use GDI Direct3D, Direct2D, or application-specific rendering technology.</span></span><br/></li>
<li><span data-ttu-id="cf950-116">Unterstützung für mehr formatieren Text.</span><span class="sxs-lookup"><span data-stu-id="cf950-116">Support for multi-format text.</span></span> <br/></li>
<li><span data-ttu-id="cf950-117">Unterstützung für die erweiterten Typografiefunktionen von OpenType-Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="cf950-117">Support for the advanced typography features of OpenType fonts.</span></span><br/></li>
<li><span data-ttu-id="cf950-118">Unterstützung für das Layout und Rendering von Text in allen Sprachen, die von Windows unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cf950-118">Support for the layout and rendering of text in all languages supported by Windows.</span></span><br/></li>
</ul>
<span data-ttu-id="cf950-119">Mit diesem SDK können Entwickler die API auswerten und grundlegende Anwendungen nur zu Demonstrationszwecken schreiben.</span><span class="sxs-lookup"><span data-stu-id="cf950-119">This SDK allows developers to evaluate the API and write basic applications for demonstration purposes only.</span></span><br/> <span data-ttu-id="cf950-120"><a href="/windows/win32/directwrite/direct-write-portal">Dokumentation</a> und <a href="/windows/win32/directwrite/samples">Beispiele</a> für DirectWrite sind zurzeit auf MSDN verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cf950-120"><a href="/windows/win32/directwrite/direct-write-portal">Documentation</a> and <a href="/windows/win32/directwrite/samples">samples</a> for DirectWrite are currently available on MSDN.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf950-121"><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1,1</span><span class="sxs-lookup"><span data-stu-id="cf950-121"><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1.1</span></span><br/></td>
<td><span data-ttu-id="cf950-122"><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1,1</a> baut auf DXGI 1,0 auf und ist für Windows Vista und Windows 7 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cf950-122"><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1.1</a> builds on DXGI 1.0 and will be available on both Windows Vista and Windows 7.</span></span> <span data-ttu-id="cf950-123">DXGI 1,1 fügt mehrere neue Features hinzu:</span><span class="sxs-lookup"><span data-stu-id="cf950-123">DXGI 1.1 adds several new features:</span></span><br/>
<ul>
<li><span data-ttu-id="cf950-124">Synchronisierte Unterstützung für freigegebene Oberflächen</span><span class="sxs-lookup"><span data-stu-id="cf950-124">Synchronized Shared Surfaces Support.</span></span> <span data-ttu-id="cf950-125">Dies ermöglicht eine effiziente Lese-und Schreib Oberflächen Freigabe zwischen mehreren D3D (möglicherweise zwischen d3d10-und D3D11-Geräten).</span><span class="sxs-lookup"><span data-stu-id="cf950-125">This enables efficient read and write surface sharing between multiple D3D (could be between D3D10 and D3D11) devices.</span></span><br/></li>
<li><span data-ttu-id="cf950-126">BGRA-Formatunterstützung.</span><span class="sxs-lookup"><span data-stu-id="cf950-126">BGRA format support.</span></span> <span data-ttu-id="cf950-127">Dies ermöglicht GDI das renderauf derselben DXGI-Oberfläche, die von einem Direct2D-, Direct3D 10,1-oder Direct3D 11-Gerät betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="cf950-127">This allows GDI to render to the same DXGI surface targeted by a Direct2D, Direct3D 10.1 or Direct3D 11 device.</span></span> <br/></li>
<li><span data-ttu-id="cf950-128">Maximale Frame Latenz.</span><span class="sxs-lookup"><span data-stu-id="cf950-128">Maximum Frame Latency.</span></span> <span data-ttu-id="cf950-129">Mithilfe von <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1:: setmaximumframelatency</strong></a> und <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1:: getmaximumframelatency</strong></a>können Titel die Anzahl der Frames steuern, die vor der Übermittlung für das Rendering in einer Warteschlange gespeichert werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="cf950-129">Using <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1::SetMaximumFrameLatency</strong></a> and <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1::GetMaximumFrameLatency</strong></a>, titles can control the number of frames that are allowed to be stored in a queue, before submission for rendering.</span></span> <span data-ttu-id="cf950-130">Latenz wird häufig verwendet, um zu steuern, wie die CPU zwischen der Reaktion auf Benutzereingaben und Frames in der geralteschlange auswählt.</span><span class="sxs-lookup"><span data-stu-id="cf950-130">Latency is often used to control how the CPU chooses between responding to user input and frames that are in the render queue.</span></span><br/></li>
<li><span data-ttu-id="cf950-131">Adapterenumeration.</span><span class="sxs-lookup"><span data-stu-id="cf950-131">Adapter Enumeration.</span></span> <span data-ttu-id="cf950-132">Mithilfe von <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1:: EnumAdapters1</strong></a>können Titel lokale Adapter ohne angehängte Monitore oder Ausgaben sowie Adapter mit verbundenen Ausgaben auflisten.</span><span class="sxs-lookup"><span data-stu-id="cf950-132">Using <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1::EnumAdapters1</strong></a>, titles can enumerates local adapters without any monitors or outputs attached, as well as adapters with outputs attached.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf950-133"><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Aktualisierte Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf950-133"><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Updated Samples</span></span><br/></td>
<td><span data-ttu-id="cf950-134">Diese Version enthält mehrere neue und aktualisierte Beispiele.</span><span class="sxs-lookup"><span data-stu-id="cf950-134">This release has several new and updated samples.</span></span><br/>
<ul>
<li><span data-ttu-id="cf950-135">Die neue <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> ist eine Abbildung erweiterter Verarbeitungsverfahren für Compute-Shader, die auf einer d3d10-oder D3D11-GPU ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="cf950-135">The new <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> is an illustration of more advanced compute shader processing techniques that can be run on a D3D10 or D3D11 GPU.</span></span></li>
<li><span data-ttu-id="cf950-136">Das <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11-Beispiel</a> wurde erweitert, um aufgrund der Verwendung von Compute-Shader (zusätzlich zur Tabellen Zuordnung) weich-und Blüten Effekte zu implementieren, und stellt für Vergleiche Pixel-Shader-Implementierungen bereit.</span><span class="sxs-lookup"><span data-stu-id="cf950-136">The <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11 sample</a> has been expanded to implement blur and bloom effects (in addition to tone mapping) using compute shader, as well as providing pixel shader implementations for comparison.</span></span></li>
<li><span data-ttu-id="cf950-137">Das <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11-Beispiel</a> wurde erheblich aktualisiert, mit komplexeren Kunst Ressourcen und einer intensiveren Thread bezogenen Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="cf950-137">The <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11 sample</a> has been significantly updated, with more complex art assets and more intensive per-thread processing.</span></span></li>
<li><span data-ttu-id="cf950-138">Das <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11-Beispiel</a> wurde mit einem neuen Gesichts Modell aktualisiert, und das Beispiel nutzt nun das Feature "featureberechnung" des Samples Content Exporter.</span><span class="sxs-lookup"><span data-stu-id="cf950-138">The <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11 sample</a> has been updated with a new facial model, and the sample now leverages the adjacency computation feature of the Samples Content Exporter.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="cf950-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cf950-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf950-140">In früheren Versionen eingeführte Features</span><span class="sxs-lookup"><span data-stu-id="cf950-140">Features Introduced In Previous Releases</span></span>](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

