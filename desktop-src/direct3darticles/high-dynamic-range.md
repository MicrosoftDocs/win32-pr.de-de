---
title: Verwenden von DirectX mit High Dynamic Range-Displays und erweiterter Farbe
description: Dieses Thema bietet eine technische Übersicht über das Rendern von Inhalten mit hoher dynamischer Breite Direct3D 11 und Direct3D 12 in eine HDR10-Anzeige mithilfe von Unterstützung für erweiterte Farben in Windows 10.
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 14d025e5431c42299c2c7f20ff198efa93959d7b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104553357"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a><span data-ttu-id="823dc-103">Verwenden von DirectX mit dynamischen Bereichs anzeigen und erweiterter Farbe</span><span class="sxs-lookup"><span data-stu-id="823dc-103">Using DirectX with high dynamic range Displays and Advanced Color</span></span>

<span data-ttu-id="823dc-104">Dieses Thema bietet eine technische Übersicht über die Ausgabe von Direct3D 11-und Direct3D 12-Inhalten in eine HDR10-Anzeige mithilfe von Unterstützung für erweiterte Farben in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="823dc-104">This topic provides a technical overview of outputting high dynamic range (HDR) Direct3D 11 and Direct3D 12 content to an HDR10 display using Windows 10 advanced color support.</span></span> <span data-ttu-id="823dc-105">Es fasst einige wichtige konzeptionelle Unterschiede zwischen der Ausgabe von HDR10 im Vergleich zu herkömmlichen standardmäßigen Dynamic Range-anzeigen (SZR) zusammen.</span><span class="sxs-lookup"><span data-stu-id="823dc-105">It summarizes some key conceptual differences between outputting to HDR10 displays as compared to traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="823dc-106">Außerdem werden die wichtigsten technischen Anforderungen für Ihre APP behandelt, um die erweiterte Windows-Farbe sowie Empfehlungen und bewährte Methoden zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="823dc-106">It also covers the key technical requirements for your app to properly support Windows advanced color, as well as recommendations and best practices.</span></span>

## <a name="introduction"></a><span data-ttu-id="823dc-107">Einführung</span><span class="sxs-lookup"><span data-stu-id="823dc-107">Introduction</span></span>

<span data-ttu-id="823dc-108">Windows 10 unterstützt HDR und andere erweiterte Farbanzeige, die eine deutlich höhere Farbgenauigkeit als herkömmliche SZR-anzeigen bieten.</span><span class="sxs-lookup"><span data-stu-id="823dc-108">Windows 10 supports HDR and other advanced color displays, which provide significantly higher color fidelity than traditional SDR displays.</span></span> <span data-ttu-id="823dc-109">Sie können "Direct3D", "Direct2D" und andere Grafik-APIs verwenden, um HDR-Inhalte in einer fähigen Anzeige darzustellen.</span><span class="sxs-lookup"><span data-stu-id="823dc-109">You can use Direct3D, Direct2D and other graphics APIs to render HDR content to a capable display.</span></span>

<span data-ttu-id="823dc-110">Die erweiterte Farbe von Windows bezieht sich auf verschiedene verwandte Technologien, die erstmals mit Windows 10 Version 1703 eingeführt wurden und Unterstützung für Anzeigefunktionen bieten, die die Farbfunktionen herkömmlicher standardmäßiger dynamischer Bereiche (SDR) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="823dc-110">Windows advanced color refers to several related technologies, first introduced with Windows 10 version 1703, that provide support for displays that exceed the color capabilities of traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="823dc-111">Die drei wichtigsten erweiterten Funktionen werden unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="823dc-111">The three major extended capabilities are described below.</span></span> <span data-ttu-id="823dc-112">Der häufigste Typ der erweiterten Farbanzeige, HDR10, unterstützt alle drei erweiterten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="823dc-112">The most common type of advanced color display, HDR10, supports all three extended capabilities.</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="823dc-113">Hoher dynamischer Bereich</span><span class="sxs-lookup"><span data-stu-id="823dc-113">High dynamic range</span></span>

<span data-ttu-id="823dc-114">Der dynamische Bereich bezieht sich auf den Unterschied zwischen der maximalen und der minimalen Leuchtkraft in einer Szene. Dies wird häufig in Nits gemessen (Kerzen-pro Quadratzentimeter).</span><span class="sxs-lookup"><span data-stu-id="823dc-114">Dynamic range refers to the difference between the maximum and minimum luminance in a scene; this is often measured in nits (candelas per square centimeter).</span></span> <span data-ttu-id="823dc-115">In realen Szenen, wie z. b. bei diesem Sonnenuntergang, gibt es häufig dynamische Bereiche mit einer Größe von mehr als einer Leuchtkraft. das menschliche Auge kann nach der Anpassung einen noch größeren Bereich erkennen.</span><span class="sxs-lookup"><span data-stu-id="823dc-115">Real world scenes, such as this sunset, often have dynamic ranges of 10 orders of magnitude of luminance; the human eye can discern an even greater range after adaptation.</span></span>

![Bild des Sonnen namens mit Helligkeit und dunkelsten Punkten in der Szene mit der Bezeichnung](images/HDR-HDR.jpg)

<span data-ttu-id="823dc-117">Seit Direct3D 9 können Grafik-Engines Ihre Szenen intern mit dieser Ebene physisch präziser Treue Renderen.</span><span class="sxs-lookup"><span data-stu-id="823dc-117">Ever since Direct3D 9, graphics engines have been able to internally render their scenes with this level of physically accurate fidelity.</span></span> <span data-ttu-id="823dc-118">Allerdings kann eine typische standardmäßige dynamische Bereichs Anzeige nur ein wenig mehr als drei Reihenfolge der Leuchtkraft reproduzieren. Daher muss jeder mit HDR gerenderte Inhalt in den begrenzten Bereich der Anzeige tonezugeordnet (komprimiert) werden.</span><span class="sxs-lookup"><span data-stu-id="823dc-118">However, a typical standard dynamic range display can reproduce only a little more than 3 orders of magnitude of luminance, and therefore any HDR-rendered content had to be tonemapped (compressed) into the limited range of the display.</span></span> <span data-ttu-id="823dc-119">Neue HDR-anzeigen, einschließlich derjenigen, die dem HDR10 (BT. 2100)-Standard entsprechen, unterbrechen diese Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="823dc-119">New HDR displays, including those that comply with the HDR10 (BT.2100) standard, break through this limitation.</span></span>

### <a name="wide-color-gamut-with-automatic-system-color-management"></a><span data-ttu-id="823dc-120">Breite Farbpalette mit automatischer System Farbverwaltung</span><span class="sxs-lookup"><span data-stu-id="823dc-120">Wide color gamut with automatic system color management</span></span>

<span data-ttu-id="823dc-121">Farb-Farbskala bezieht sich auf den Bereich und die Sättigung der Schattierungen, die eine Anzeige reproduzieren kann.</span><span class="sxs-lookup"><span data-stu-id="823dc-121">Color gamut refers to the range and saturation of hues that a display can reproduce.</span></span> <span data-ttu-id="823dc-122">Die gebräuchlichste natürliche Farbe, die das menschliche Auge erkennen kann, ist rein, Monochromatisch, wie z. b. das, was von einem Laser erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="823dc-122">The most saturated natural color the human eye can perceive is pure, monochromatic light such as what is produced by a laser.</span></span> <span data-ttu-id="823dc-123">Allerdings können gängige Consumer-anzeigen häufig Farben nur innerhalb des sRGB-Gamut reproduzieren, der nur ungefähr 35% aller von Menschen wahrnehmbaren Farben darstellt.</span><span class="sxs-lookup"><span data-stu-id="823dc-123">However, mainstream consumer displays can often reproduce colors only within the sRGB gamut, which represents only about 35% of all human-perceivable colors.</span></span> <span data-ttu-id="823dc-124">Das folgende Diagramm ist eine Darstellung des menschlichen "spektralen Lokus" oder aller wahrnehmbaren Farben (auf einer bestimmten Beleuchtungs Ebene), wobei das kleinere Dreieck der sRGB-Gamut ist.</span><span class="sxs-lookup"><span data-stu-id="823dc-124">The diagram below is a representation of the human "spectral locus", or all perceivable colors (at a given luminance level), where the smaller triangle is the sRGB gamut.</span></span>

![Diagramm des menschlichen spektralen Lokus und sRGB-Farbskala](images/HDR-WCG.jpg)

<span data-ttu-id="823dc-126">High-End, die Professional PC-Anzeige hat lange unterstützte Farbspiele, die deutlich breiter als sRGB sind, z. b. Adobe RGB und D65-P3.</span><span class="sxs-lookup"><span data-stu-id="823dc-126">High end, professional PC displays have long supported color gamuts that are significantly wider than sRGB, such as Adobe RGB and D65-P3.</span></span> <span data-ttu-id="823dc-127">Diese großen Fenster anzeigen werden immer häufiger.</span><span class="sxs-lookup"><span data-stu-id="823dc-127">And these wide gamut displays are becoming more common.</span></span> <span data-ttu-id="823dc-128">Vor der erweiterten Farbe hat Windows jedoch keine Farbverwaltung auf Systemebene für Anwendungen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="823dc-128">However, prior to advanced color, Windows didn't perform any system-level color management for applications.</span></span> <span data-ttu-id="823dc-129">Dies bedeutete, dass Windows beim Rendern einer DirectX-APP, z. b. eines reinen roten oder RGB (1.0, 0,0, 0,0) in seine Swapkette, einfach das am stärksten satte rote Abbild Scannen konnte, das die Darstellung reproduzieren konnte, unabhängig davon, was der tatsächliche Farbverlauf der Anzeige war.</span><span class="sxs-lookup"><span data-stu-id="823dc-129">This meant that if a DirectX app rendered, for example, a pure red or RGB(1.0, 0.0, 0.0) to its swap chain, then Windows would simply scan out the most saturated red that the display could reproduce, regardless of what the actual color gamut of the display was.</span></span>

<span data-ttu-id="823dc-130">Apps, die eine hohe Farbgenauigkeit benötigten, konnten die Farbfunktionen der Anzeige Abfragen (z. b. mithilfe von "ICC-Profilen") und eine eigene Prozess interne Farbverwaltung durchführen, um den Farbverlauf der Anzeige ordnungsgemäß zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="823dc-130">Apps that needed high color accuracy could query the color capabilities of the display (for example, using ICC profiles), and perform their own in-process color management to correctly target the display's color gamut.</span></span> <span data-ttu-id="823dc-131">Bei den meisten apps und visuellen Inhalten wird jedoch davon ausgegangen, dass die Anzeige sRGB ist, und Sie verlassen sich auf das Betriebssystem, um diese Annahme zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="823dc-131">However, the vast majority of apps and visual content assume that the display is sRGB, and they rely on the operating system to fulfill this assumption.</span></span>

<span data-ttu-id="823dc-132">Die erweiterte Windows-Farbe fügt eine automatische Farbverwaltung auf Systemebene hinzu.</span><span class="sxs-lookup"><span data-stu-id="823dc-132">Windows advanced color adds automatic system-level color management.</span></span> <span data-ttu-id="823dc-133">Der Desktopfenster-Manager (DWM) ist Windows-Compositor.</span><span class="sxs-lookup"><span data-stu-id="823dc-133">The Desktop Window Manager (DWM) is Windows' compositor.</span></span> <span data-ttu-id="823dc-134">Wenn erweiterte Farbe aktiviert ist, führt die DWM eine explizite Farbkonvertierung aus dem colorspace-Element der visuellen app in einen kanonischen Kompositions Farbraum durch, bei dem es sich um ScRGB handelt.</span><span class="sxs-lookup"><span data-stu-id="823dc-134">When advanced color is enabled, the DWM performs an explicit color conversion from the app visual content's colorspace to a canonical composition color space, which is scRGB.</span></span> <span data-ttu-id="823dc-135">Windows konvertiert dann den zusammengesetzten Frame Puffer-Inhalt in den nativen Farbraum der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="823dc-135">Windows then color-converts the composed framebuffer content to the display's native color space.</span></span> <span data-ttu-id="823dc-136">Auf diese Weise erhält herkömmliche sRGB-Inhalte automatisch ein Farb genaues Verhalten, während erweiterte Farb abhängige Apps die vollständigen Farbfunktionen der Anzeige nutzen können.</span><span class="sxs-lookup"><span data-stu-id="823dc-136">In this way, traditional sRGB content automatically gets color-accurate behavior, while advanced color-aware apps can take advantage of the full color capabilities of the display.</span></span>

### <a name="deep-precisionbit-depth"></a><span data-ttu-id="823dc-137">Tiefe Genauigkeit/Bittiefe</span><span class="sxs-lookup"><span data-stu-id="823dc-137">Deep precision/bit depth</span></span>

<span data-ttu-id="823dc-138">Die numerische Genauigkeit oder die Bittiefe bezieht sich auf das darstellen oder unterscheiden zwischen ähnlichen, aber unterschiedlichen Farben ohne Bandbreite und Artefakte.</span><span class="sxs-lookup"><span data-stu-id="823dc-138">Numerical precision, or bit depth, refers to representing or distinguishing between similar but distinct colors without banding nor artifacts.</span></span> <span data-ttu-id="823dc-139">Der Mainstream-PC zeigt Unterstützung für 8 Bits pro Farbkanal an, während für das menschliche Auge mindestens 10-12 Bits an Genauigkeit erforderlich sind, um wahrnehmbare Verzerrungen zu vermeiden, ohne auf Techniken wie Dithering oder die Anzeige Bedingungen zurückgreifen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="823dc-139">Mainstream PC displays support 8 bits per color channel, while the human eye requires at least 10-12 bits of precision to avoid perceivable distortions, without resorting to techniques such as dithering or depending on viewing conditions.</span></span>

![Bild von Windmühlen mit simulierten 2 Bits pro Farbkanal und 8 Bits pro Kanal](images/HDR-bitdepth.jpg)

<span data-ttu-id="823dc-141">Vor der erweiterten Farbe haben die DWM-Anwendungen eingeschränkt, um Inhalt nur in 8 Bits pro Farbkanal auszugeben, auch wenn die Anzeige eine höhere Bitrate unterstützte.</span><span class="sxs-lookup"><span data-stu-id="823dc-141">Prior to advanced color, the DWM restricted windowed apps to output content at only 8 bits per color channel, even if the display supported a higher bit depth.</span></span> <span data-ttu-id="823dc-142">Wenn erweiterte Farbe aktiviert ist, führt die DWM die Komposition mithilfe des IEEE-Werts mit halber Genauigkeit (FP16) aus, um Engpässe zu beseitigen und die Verwendung der vollständigen Genauigkeit der Anzeige zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="823dc-142">When advanced color is enabled, the DWM performs its composition using IEEE half-precision floating point (FP16), eliminating any bottlenecks, and allowing the full precision of the display to be used.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="823dc-143">Systemanforderungen</span><span class="sxs-lookup"><span data-stu-id="823dc-143">System Requirements</span></span>

### <a name="operating-system-os"></a><span data-ttu-id="823dc-144">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="823dc-144">Operating system (OS)</span></span>

<span data-ttu-id="823dc-145">Die erweiterte Farbunterstützung ist zuerst mit Windows 10, Version 1703, ausgeliefert und wurde bei jedem Update erheblich verbessert.</span><span class="sxs-lookup"><span data-stu-id="823dc-145">Advanced color support first shipped with Windows 10, version 1703, and it has been significantly improved with each update.</span></span> <span data-ttu-id="823dc-146">In diesem Thema wird davon ausgegangen, dass Ihre APP auf Windows 10, Version 1903 oder höher, abzielt.</span><span class="sxs-lookup"><span data-stu-id="823dc-146">This topic assumes that your app is targeting Windows 10, version 1903, or later.</span></span>

### <a name="display"></a><span data-ttu-id="823dc-147">Anzeige</span><span class="sxs-lookup"><span data-stu-id="823dc-147">Display</span></span>

<span data-ttu-id="823dc-148">Um einen hohen dynamischen Bereich zu nutzen, müssen Sie über eine Anzeige verfügen, die den HDR10-Standard unterstützt.</span><span class="sxs-lookup"><span data-stu-id="823dc-148">To take advantage of high dynamic range, you must have a display that supports the HDR10 standard.</span></span> <span data-ttu-id="823dc-149">Windows funktioniert am besten mit anzeigen, die [VESA displayhdr-zertifiziert](https://displayhdr.org/)sind.</span><span class="sxs-lookup"><span data-stu-id="823dc-149">Windows works best with displays that are [VESA DisplayHDR certified](https://displayhdr.org/).</span></span>

### <a name="graphics-processor-gpu"></a><span data-ttu-id="823dc-150">Grafikprozessor (GPU)</span><span class="sxs-lookup"><span data-stu-id="823dc-150">Graphics processor (GPU)</span></span>

<span data-ttu-id="823dc-151">Eine aktuelle GPU ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="823dc-151">A recent GPU is required.</span></span> <span data-ttu-id="823dc-152">Zur Unterstützung von HDR10-anzeigen erfordert Windows 10 einen der folgenden Punkte.</span><span class="sxs-lookup"><span data-stu-id="823dc-152">To support HDR10 displays, Windows 10 requires one of the following.</span></span>

* <span data-ttu-id="823dc-153">NVIDIA GeForce 1000-Serie (Pascal) oder neuer</span><span class="sxs-lookup"><span data-stu-id="823dc-153">Nvidia GeForce 1000 series (Pascal), or newer</span></span>
* <span data-ttu-id="823dc-154">AMD Radeon RX 400 Series (Polaris) oder neuer</span><span class="sxs-lookup"><span data-stu-id="823dc-154">AMD Radeon RX 400 series (Polaris), or newer</span></span>
* <span data-ttu-id="823dc-155">Ausgewählte Intel Core 7-Serie (kaby Lake) oder höher</span><span class="sxs-lookup"><span data-stu-id="823dc-155">Selected Intel Core 7 series (Kaby Lake), or newer</span></span>

<span data-ttu-id="823dc-156">Beachten Sie, dass abhängig von den Szenarien, einschließlich Hardware-Codec-Beschleunigung (10 Bit hevc, 10 Bit VP9 usw.) und PlayReady-Unterstützung (SL3000), zusätzliche Hardwareanforderungen gelten.</span><span class="sxs-lookup"><span data-stu-id="823dc-156">Note that additional hardware requirements apply depending on the scenarios, including hardware codec acceleration (10 bit HEVC, 10 bit VP9, etc.) and PlayReady support (SL3000).</span></span> <span data-ttu-id="823dc-157">Weitere Informationen erhalten Sie von Ihrem GPU-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="823dc-157">Contact your GPU vendor for more specific information.</span></span>

### <a name="graphics-driver-wddm"></a><span data-ttu-id="823dc-158">Grafiktreiber (WDDM)</span><span class="sxs-lookup"><span data-stu-id="823dc-158">Graphics driver (WDDM)</span></span>

<span data-ttu-id="823dc-159">Der neueste verfügbare Grafiktreiber wird dringend empfohlen, entweder von Windows Update oder vom GPU-Hersteller oder von der Website des PC-Herstellers.</span><span class="sxs-lookup"><span data-stu-id="823dc-159">The latest available graphics driver is strongly recommended, either from Windows Update or from the GPU vendor or PC manufacturer's website.</span></span> <span data-ttu-id="823dc-160">Für Windows 10, Version 1903 und höher, empfehlen wir Treiber, die mindestens Windows Display Driver Model (WDDM), Version 2,6, unterstützen.</span><span class="sxs-lookup"><span data-stu-id="823dc-160">For Windows 10, version 1903, and later, we recommend drivers that support at least Windows Display Driver Model (WDDM) version 2.6.</span></span>

## <a name="supported-rendering-apis"></a><span data-ttu-id="823dc-161">Unterstützte Rendering-APIs</span><span class="sxs-lookup"><span data-stu-id="823dc-161">Supported rendering APIs</span></span>

<span data-ttu-id="823dc-162">Windows 10 unterstützt eine Vielzahl von renderingapis und Frameworks.</span><span class="sxs-lookup"><span data-stu-id="823dc-162">Windows 10 supports a wide variety of rendering APIs and frameworks.</span></span> <span data-ttu-id="823dc-163">Die erweiterte Farbunterstützung basiert im Grunde darauf, dass Ihre APP eine moderne Präsentation mit DXGI oder den APIs der visuellen Ebene durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="823dc-163">Advanced color support fundamentally relies on your app being able to perform modern presentation using either DXGI or the Visual Layer APIs.</span></span>

* [<span data-ttu-id="823dc-164">DirectX-Grafik Infrastruktur (DXGI)</span><span class="sxs-lookup"><span data-stu-id="823dc-164">DirectX Graphics Infrastructure (DXGI)</span></span>](../direct3ddxgi/dx-graphics-dxgi.md)
* [<span data-ttu-id="823dc-165">Visuelle Ebene (Windows. UI. Composition)</span><span class="sxs-lookup"><span data-stu-id="823dc-165">Visual Layer (Windows.UI.Composition)</span></span>](/windows/uwp/composition/visual-layer)

<span data-ttu-id="823dc-166">Daher kann jede Rendering-API, die eine dieser Präsentationsmethoden ausgeben kann, die erweiterte Farbe unterstützen.</span><span class="sxs-lookup"><span data-stu-id="823dc-166">Therefore, any rendering API that can output to one of these presentations methods can support advanced color.</span></span> <span data-ttu-id="823dc-167">Dies umfasst u. a. die folgenden.</span><span class="sxs-lookup"><span data-stu-id="823dc-167">This includes but is not limited to these.</span></span>

* [<span data-ttu-id="823dc-168">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="823dc-168">Direct3D 11</span></span>](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [<span data-ttu-id="823dc-169">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="823dc-169">Direct3D 12</span></span>](../direct3d12/direct3d-12-graphics.md)
* [<span data-ttu-id="823dc-170">Direct2D</span><span class="sxs-lookup"><span data-stu-id="823dc-170">Direct2D</span></span>](../direct2d/direct2d-portal.md)
* [<span data-ttu-id="823dc-171">Win2D</span><span class="sxs-lookup"><span data-stu-id="823dc-171">Win2D</span></span>](https://github.com/Microsoft/Win2D)
  * <span data-ttu-id="823dc-172">Erfordert die Verwendung der **kanvasswapchain** -oder **canvasswapchainpanel** -APIs auf niedrigerer Ebene.</span><span class="sxs-lookup"><span data-stu-id="823dc-172">Requires using the lower level **CanvasSwapChain** or **CanvasSwapChainPanel** APIs.</span></span>
* [<span data-ttu-id="823dc-173">**Windows.UI.Input.Inking**</span><span class="sxs-lookup"><span data-stu-id="823dc-173">**Windows.UI.Input.Inking**</span></span>](/uwp/api/Windows.UI.Input.Inking)
  * <span data-ttu-id="823dc-174">Unterstützt das benutzerdefinierte Dry Ink-Rendering mit DirectX.</span><span class="sxs-lookup"><span data-stu-id="823dc-174">Supports custom dry ink rendering using DirectX.</span></span>
* [<span data-ttu-id="823dc-175">XAML</span><span class="sxs-lookup"><span data-stu-id="823dc-175">XAML</span></span>](/windows/uwp/xaml-platform/)
  * <span data-ttu-id="823dc-176">Unterstützt die Wiedergabe von HDR-Videos mithilfe von **mediaplayerelement**.</span><span class="sxs-lookup"><span data-stu-id="823dc-176">Supports playback of HDR videos using **MediaPlayerElement**.</span></span>
  * <span data-ttu-id="823dc-177">Unterstützt die Decodierung von JPEG XR-Bildern mithilfe des **Image** -Elements.</span><span class="sxs-lookup"><span data-stu-id="823dc-177">Supports decode of JPEG XR images using **Image** element.</span></span>
  * <span data-ttu-id="823dc-178">Unterstützt DirectX-Interop mithilfe von " **Swap-chainpanel**".</span><span class="sxs-lookup"><span data-stu-id="823dc-178">Supports DirectX interop using **SwapChainPanel**.</span></span>

## <a name="handling-dynamic-display-capabilities"></a><span data-ttu-id="823dc-179">Behandeln dynamischer Anzeigefunktionen</span><span class="sxs-lookup"><span data-stu-id="823dc-179">Handling dynamic display capabilities</span></span>

<span data-ttu-id="823dc-180">Windows 10 unterstützt eine große Bandbreite von erweiterten Farb fähigen anzeigen, von energieeffizienten integrierten Panels bis hin zu High-End-Gaming-Monitoren und-fern.</span><span class="sxs-lookup"><span data-stu-id="823dc-180">Windows 10 supports an enormous range of advanced color-capable displays, from power-efficient integrated panels to high end gaming monitors and TVs.</span></span> <span data-ttu-id="823dc-181">Windows-Benutzer erwarten, dass Ihre APP alle diese Variationen nahtlos verarbeitet, einschließlich der universellen vorhandenen SZR-Anzeige.</span><span class="sxs-lookup"><span data-stu-id="823dc-181">Windows users expect that your app will seamlessly handle all of these variations, including ubiquitous existing SDR displays.</span></span>

<span data-ttu-id="823dc-182">Windows 10 bietet dem Benutzer die Kontrolle über die Funktionen von HDR und erweiterten Farben.</span><span class="sxs-lookup"><span data-stu-id="823dc-182">Windows 10 provides control over HDR and advanced color capabilities to the user.</span></span> <span data-ttu-id="823dc-183">Ihre APP muss die Konfiguration der aktuellen Anzeige erkennen und dynamisch auf alle Änderungen reagieren.</span><span class="sxs-lookup"><span data-stu-id="823dc-183">Your app must detect the current display's configuration, and respond dynamically to any changes in capability.</span></span> <span data-ttu-id="823dc-184">Dies kann verschiedene Ursachen haben, z. b. weil der Benutzer eine Funktion aktiviert oder deaktiviert oder die APP zwischen verschiedenen anzeigen verschoben hat oder sich der Energiezustand des Systems geändert hat.</span><span class="sxs-lookup"><span data-stu-id="823dc-184">This could occur for many reasons, for example, because the user enabled or disabled a feature, or moved the app between different displays, or the system's power state changed.</span></span>

### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="823dc-185">Universelle Windows-Plattform-Apps (UWP)</span><span class="sxs-lookup"><span data-stu-id="823dc-185">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="823dc-186">Wenn Sie eine UWP-app schreiben, verwenden Sie, unabhängig von der verwendeten Grafik Rendering-API, [**advancedcolorinfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) , um Anzeigefunktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="823dc-186">If you're writing a UWP app, regardless of the graphics rendering API you're using, use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get display capabilities.</span></span> <span data-ttu-id="823dc-187">Rufen Sie eine Instanz von **advancedcolorinfo** aus [**Displayinformation:: getadvancedcolorinfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo)ab.</span><span class="sxs-lookup"><span data-stu-id="823dc-187">Obtain an instance of **AdvancedColorInfo** from [**DisplayInformation::GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).</span></span>

<span data-ttu-id="823dc-188">Verwenden Sie die [**currentadvancedcolorkind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) -Eigenschaft, um zu überprüfen, welche erweiterte Farbart derzeit aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="823dc-188">To check what advanced color kind is currently active, use the [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) property.</span></span> <span data-ttu-id="823dc-189">In Windows 10, Version 1903 und höher, wird ein von drei möglichen Werten zurückgegeben: " **SZR**", " **WCG**" oder " **HDR**".</span><span class="sxs-lookup"><span data-stu-id="823dc-189">In Windows 10, version 1903, and later, this returns one of three possible values: **SDR**, **WCG**, or **HDR**.</span></span> <span data-ttu-id="823dc-190">Dies ist die wichtigste zu Überprüfung, und Sie sollten die Renderingpipeline und die Präsentations Pipeline als Reaktion auf die aktive Art konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="823dc-190">This is the most important property to check, and you should configure your render and presentation pipeline in response to the active kind.</span></span>

<span data-ttu-id="823dc-191">Um zu überprüfen, welche erweiterten Farb Arten unterstützt werden, aber nicht unbedingt aktiv sind, wenden Sie [**isadvancedcolorkindavailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable)an.</span><span class="sxs-lookup"><span data-stu-id="823dc-191">To check what advanced color kinds are supported, but not necessarily active, call [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable).</span></span> <span data-ttu-id="823dc-192">Sie können diese Informationen z. b. verwenden, um den Benutzer zur Eingabe der Windows-Einstellungs-APP aufzufordern, damit Sie HDR oder WCG aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="823dc-192">You could use this information, for example, to prompt the user to navigate to the Windows Settings app so that they can enable HDR or WCG.</span></span>

<span data-ttu-id="823dc-193">Die anderen Mitglieder von **advancedcolorinfo** stellen quantitative Informationen über das physische Farbvolumen des Panels ("Leuchtkraft" und "Chrominance") bereit, die den statischen HDR-Metadaten von SMPTE St. 2086 entsprechen.</span><span class="sxs-lookup"><span data-stu-id="823dc-193">The other members of **AdvancedColorInfo** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="823dc-194">Sie sollten diese Informationen verwenden, um die HDR Tonemapping-und Farbskala-Zuordnung Ihrer APP zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="823dc-194">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="823dc-195">Registrieren Sie sich für das [**advancedcolorinfochanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) -Ereignis, um Änderungen in erweiterten Farbfunktionen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="823dc-195">To handle changes in advanced color capabilities, register for the [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) event.</span></span> <span data-ttu-id="823dc-196">Dieses Ereignis wird ausgelöst, wenn sich ein Parameter der erweiterten Farbfunktionen der Anzeige aus irgendeinem Grund ändert.</span><span class="sxs-lookup"><span data-stu-id="823dc-196">This event is raised if any parameter of the display's advanced color capabilities changes for any reason.</span></span>

<span data-ttu-id="823dc-197">Behandeln Sie dieses Ereignis, indem Sie eine neue Instanz von **advancedcolorinfo** abrufen und überprüfen, welche Werte geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="823dc-197">Handle this event by obtaining a new instance of **AdvancedColorInfo**, and checking which values have changed.</span></span>

### <a name="desktop-win32-directx-apps"></a><span data-ttu-id="823dc-198">Desktop-DirectX-Apps (Win32)</span><span class="sxs-lookup"><span data-stu-id="823dc-198">Desktop (Win32) DirectX apps</span></span>

<span data-ttu-id="823dc-199">Wenn Sie eine Win32-app schreiben und DirectX zum Renderingvorgang verwenden, verwenden Sie [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) , um Anzeigefunktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="823dc-199">If you're writing a Win32 app, and using DirectX to render, then use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get display capabilities.</span></span> <span data-ttu-id="823dc-200">Rufen Sie eine Instanz dieser Struktur über [**IDXGIOutput6:: GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1)ab.</span><span class="sxs-lookup"><span data-stu-id="823dc-200">Obtain an instance of this struct via [**IDXGIOutput6::GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).</span></span>

<span data-ttu-id="823dc-201">Um zu überprüfen, welche erweiterte Farbart derzeit aktiv ist, verwenden Sie die **colorspace** -Eigenschaft, die vom Typ [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)ist, und enthält einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="823dc-201">To check what advanced color kind is currently active, use the **ColorSpace** property, which is of type [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), and contains one of the following values:</span></span>

* <span data-ttu-id="823dc-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span><span class="sxs-lookup"><span data-stu-id="823dc-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span></span>
* <span data-ttu-id="823dc-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span><span class="sxs-lookup"><span data-stu-id="823dc-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span></span>

> [!Note]
> <span data-ttu-id="823dc-204">Andere erweiterte Farb Arten, wie z. b. WCG, werden von DXGI als SZR behandelt.</span><span class="sxs-lookup"><span data-stu-id="823dc-204">Other advanced color kinds such as WCG are treated as SDR by DXGI.</span></span> <span data-ttu-id="823dc-205">DXGI kann nicht verwendet werden, um eine WCG-Anzeige zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="823dc-205">You can't use DXGI to identify a WCG display.</span></span>

> [!Note]
> <span data-ttu-id="823dc-206">Mit DXGI können Sie nicht überprüfen, welche erweiterten Farb Arten unterstützt werden, aber derzeit nicht aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="823dc-206">DXGI doesn't let you check what advanced color kinds are supported but not active at the moment.</span></span>

<span data-ttu-id="823dc-207">Die meisten anderen Member von **DXGI_OUTPUT_DESC1** stellen quantitative Informationen über das physische Farbvolumen des Panels ("Leuchtkraft" und "Chrominance") bereit, die den statischen HDR-Metadaten von SMPTE St. 2086 entsprechen.</span><span class="sxs-lookup"><span data-stu-id="823dc-207">Most of the other members of **DXGI_OUTPUT_DESC1** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="823dc-208">Sie sollten diese Informationen verwenden, um die HDR Tonemapping-und Farbskala-Zuordnung Ihrer APP zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="823dc-208">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="823dc-209">Win32-apps verfügen über keinen systemeigenen Mechanismus zum reagieren auf Erweiterte Farb Funktionsänderungen.</span><span class="sxs-lookup"><span data-stu-id="823dc-209">Win32 apps don't have a native mechanism to respond to advanced color capability changes.</span></span> <span data-ttu-id="823dc-210">Wenn Ihre APP eine Renderschleife verwendet, sollten Sie stattdessen [**IDXGIFactory1:: IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) mit jedem Frame Abfragen.</span><span class="sxs-lookup"><span data-stu-id="823dc-210">Instead, if your app uses a render loop, then you should query [**IDXGIFactory1::IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) with each frame.</span></span> <span data-ttu-id="823dc-211">Wenn **false** angezeigt wird, sollten Sie eine neue **DXGI_OUTPUT_DESC1** abrufen und überprüfen, welche Werte geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="823dc-211">If it reports **FALSE**, then you should obtain a new **DXGI_OUTPUT_DESC1**, and check which values have changed.</span></span>

<span data-ttu-id="823dc-212">Außerdem sollte die Win32-Nachrichten Pumpe die [**WM_SIZE**](../winmsg/wm-size.md) Nachricht verarbeiten, die darauf hinweist, dass Ihre APP möglicherweise zwischen verschiedenen anzeigen verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="823dc-212">In addition, your Win32 message pump should handle the [**WM_SIZE**](../winmsg/wm-size.md) message, which indicates that your app may have moved between different displays.</span></span>

> [!Note]
> <span data-ttu-id="823dc-213">Zum Abrufen eines neuen **DXGI_OUTPUT_DESC1** müssen Sie die aktuelle Anzeige abrufen.</span><span class="sxs-lookup"><span data-stu-id="823dc-213">To obtain a new **DXGI_OUTPUT_DESC1**, you must obtain the current display.</span></span> <span data-ttu-id="823dc-214">Allerdings sollten Sie **idxgiswapchain:: getcontainingoutput** nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="823dc-214">However, you should not call **IDXGISwapChain::GetContainingOutput**.</span></span> <span data-ttu-id="823dc-215">Dies liegt daran, dass Swapketten eine veraltete DXGI-Ausgabe zurückgeben, sobald **dxgifactory:: IsCurrent** false ist, und wenn die SwapChain neu erstellt wird, um eine aktuelle Ausgabe zu erhalten, wird ein temporärer schwarzer Bildschirm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="823dc-215">This is because swap chains will return a stale DXGI output once **DXGIFactory::IsCurrent** is false, and recreating the swap chain to get a current output results in a temporary black screen.</span></span> <span data-ttu-id="823dc-216">Stattdessen wird empfohlen, die Grenzen aller DXGI-Ausgaben aufzulisten und zu bestimmen, welche Schnittmenge mit den Begrenzungen Ihres App-Fensters am größten ist.</span><span class="sxs-lookup"><span data-stu-id="823dc-216">Instead, we recommend that you enumerate through the bounds of all DXGI outputs, and determine which one has the greatest intersection with your app window's bounds.</span></span>

<span data-ttu-id="823dc-217">Das folgende Codebeispiel stammt aus dem [Repository DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="823dc-217">The following code example comes from the [DirectX-Graphics-Samples repository](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span>

```cpp
// Retrieve the current default adapter.
ComPtr<IDXGIAdapter1> dxgiAdapter;
ThrowIfFailed(m_dxgiFactory->EnumAdapters1(0, &dxgiAdapter));

// Iterate through the DXGI outputs associated with the DXGI adapter,
// and find the output whose bounds have the greatest overlap with the
// app window (i.e. the output for which the intersection area is the
// greatest).

UINT i = 0;
ComPtr<IDXGIOutput> currentOutput;
ComPtr<IDXGIOutput> bestOutput;
float bestIntersectArea = -1;

while (dxgiAdapter->EnumOutputs(i, &currentOutput) != DXGI_ERROR_NOT_FOUND)
{
    // Get the retangle bounds of the app window
    int ax1 = m_windowBounds.left;
    int ay1 = m_windowBounds.top;
    int ax2 = m_windowBounds.right;
    int ay2 = m_windowBounds.bottom;

    // Get the rectangle bounds of current output
    DXGI_OUTPUT_DESC desc;
    ThrowIfFailed(currentOutput->GetDesc(&desc));
    RECT r = desc.DesktopCoordinates;
    int bx1 = r.left;
    int by1 = r.top;
    int bx2 = r.right;
    int by2 = r.bottom;

    // Compute the intersection
    int intersectArea = ComputeIntersectionArea(ax1, ay1, ax2, ay2, bx1, by1, bx2, by2);
    if (intersectArea > bestIntersectArea)
    {
        bestOutput = currentOutput;
        bestIntersectArea = static_cast<float>(intersectArea);
    }

    i++;
}

// Having determined the output (display) upon which the app is primarily being 
// rendered, retrieve the HDR capabilities of that display by checking the color space.
ComPtr<IDXGIOutput6> output6;
ThrowIfFailed(bestOutput.As(&output6));

DXGI_OUTPUT_DESC1 desc1;
ThrowIfFailed(output6->GetDesc1(&desc1));
```

## <a name="setting-up-your-directx-swap-chain"></a><span data-ttu-id="823dc-218">Einrichten der DirectX-Swap-Kette</span><span class="sxs-lookup"><span data-stu-id="823dc-218">Setting up Your DirectX swap chain</span></span>

<span data-ttu-id="823dc-219">Nachdem Sie festgestellt haben, dass die Anzeige derzeit erweiterte Farbfunktionen unterstützt, konfigurieren Sie die Swapkette wie folgt.</span><span class="sxs-lookup"><span data-stu-id="823dc-219">Once you have determined that the display currently supports advanced color capabilities, configure your swap chain as follows.</span></span>

### <a name="use-a-flip-presentation-model-effect"></a><span data-ttu-id="823dc-220">Verwenden eines Flip Presentation Model-Effekts</span><span class="sxs-lookup"><span data-stu-id="823dc-220">Use a flip presentation model effect</span></span>

<span data-ttu-id="823dc-221">Beim Erstellen der **SwapChain mithilfe von "fiateswapchainfor" [HWND | Komposition | Corewindow]** -Methoden. Sie müssen das DXGI-Flip-Modell verwenden, indem Sie entweder die Option " **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** " oder " **DXGI_SWAP_EFFECT_FLIP_DISCARD** " auswählen, wodurch die SwapChain für die erweiterte Farbverarbeitung von DWM und verschiedene voll Bild Optimierungen geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="823dc-221">When creating your swap chain using the **CreateSwapChainFor[Hwnd|Composition|CoreWindow]** methods, you must use the DXGI flip model by selecting either the **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** or **DXGI_SWAP_EFFECT_FLIP_DISCARD** option, which makes your swap chain eligible for advanced color processing from DWM and various fullscreen optimizations.</span></span> <span data-ttu-id="823dc-222">Weitere Informationen finden Sie im Thema [zur optimalen Leistung und zum Verwenden des DXGI-Flip-Modells](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) .</span><span class="sxs-lookup"><span data-stu-id="823dc-222">For more information, refer to the [For best performance, use DXGI flip model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) topic.</span></span>

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a><span data-ttu-id="823dc-223">Option 1.</span><span class="sxs-lookup"><span data-stu-id="823dc-223">Option 1.</span></span> <span data-ttu-id="823dc-224">FP16-Pixel Format und ScRGB-Farbraum verwenden</span><span class="sxs-lookup"><span data-stu-id="823dc-224">Use FP16 pixel format and scRGB color space</span></span>

<span data-ttu-id="823dc-225">Windows 10 unterstützt zwei Haupt Kombinationen von Pixel Format und Farbraum für erweiterte Farben.</span><span class="sxs-lookup"><span data-stu-id="823dc-225">Windows 10 supports two main combinations of pixel format and color space for advanced color.</span></span> <span data-ttu-id="823dc-226">Wählen Sie einen basierend auf den spezifischen Anforderungen Ihrer APP aus.</span><span class="sxs-lookup"><span data-stu-id="823dc-226">Select one based on your app's specific requirements.</span></span>

<span data-ttu-id="823dc-227">Für allgemeine apps empfiehlt es sich beim Erstellen der SwapChain, [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)anzugeben.</span><span class="sxs-lookup"><span data-stu-id="823dc-227">For general-purpose apps, when creating your swap chain we recommend specifying [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="823dc-228">Dies wird auch als *FP16* in Ihrer [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="823dc-228">That's also known as *FP16* in your [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="823dc-229">Standardmäßig wird eine Austausch Kette, die mit einem Gleit Komma-Pixel Format erstellt wurde, so behandelt, als ob Sie den [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) Farbraum verwendet, der auch als *ScRGB* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="823dc-229">By default, a swap chain created with a floating point pixel format is treated as if it uses the [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) color space, which is also known as *scRGB*.</span></span>

<span data-ttu-id="823dc-230">Diese Kombination ermöglicht Ihnen den numerischen Bereich und die Genauigkeit, um nahezu jede physisch mögliche Farbe anzugeben und eine beliebige Verarbeitung einschließlich der Mischung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="823dc-230">This combination provides you with the numeric range and precision to specify almost any physically possible color, and perform arbitrary processing including blending.</span></span> <span data-ttu-id="823dc-231">Wenn Sie Direct2D, Win2D oder Windows. UI. Composition verwenden, ist dies die einzige unterstützte Kombination für alle Austausch Ketten oder Zwischenziele, die erweiterte Farb Inhalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="823dc-231">In addition, if you're using Direct2D, Win2D, or Windows.UI.Composition, then this is the only supported combination for any swap chain or intermediate target that contains advanced color content.</span></span> 

<span data-ttu-id="823dc-232">Der wichtigste Nachteil dieser Option besteht darin, dass Sie 64 Bits pro Pixel verbraucht, wodurch die GPU-Bandbreite und der Arbeitsspeicher Verbrauch im Vergleich zu den herkömmlichen Uint8 SZR-Pixel Formaten verdoppelt werden.</span><span class="sxs-lookup"><span data-stu-id="823dc-232">The main tradeoff of this option is that it consumes 64 bits per pixel, which doubles GPU bandwidth and memory consumption compared to the traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="823dc-233">Außerdem verwendet ScRGB numerische Werte außerhalb des normalisierten [0, 1]-Bereichs zur Darstellung von Farben außerhalb der sRGB-Farbskala und/oder mehr als 80 Nits der Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="823dc-233">In addition, scRGB uses numeric values that are outside the normalized [0, 1] range to represent colors that are outside the sRGB gamut and/or greater than 80 nits of luminance.</span></span> <span data-ttu-id="823dc-234">ScRGB (1,0, 1,0, 1,0) codiert z. b. den standardmäßigen D65 White bei 80 Nits. ScRGB (12,5, 12,5, 12,5) codiert jedoch dasselbe D65 weiß bei einem wesentlich helleren 1000-Nits.</span><span class="sxs-lookup"><span data-stu-id="823dc-234">For example, scRGB (1.0, 1.0, 1.0) encodes the standard D65 white at 80 nits; but scRGB (12.5, 12.5, 12.5) encodes the same D65 white at a much brighter 1000 nits.</span></span> <span data-ttu-id="823dc-235">Für einige Grafik Vorgänge ist ein normalisierter numerischer Bereich erforderlich, und Sie müssen den Vorgang entweder ändern oder die Farbwerte erneut normalisieren.</span><span class="sxs-lookup"><span data-stu-id="823dc-235">Some graphics operations require a normalized numeric range, and you must either modify the operation, or re-normalize color values.</span></span>

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a><span data-ttu-id="823dc-236">Option 2: Verwenden des UINT10/RGB10-Pixel Formats und des HDR10/BT. 2100-Farbraum</span><span class="sxs-lookup"><span data-stu-id="823dc-236">Option 2: Use UINT10/RGB10 pixel format and HDR10/BT.2100 color space</span></span>

<span data-ttu-id="823dc-237">Für apps, die HDR10-codierten Inhalt verwenden, z. b. Medien Player, oder apps, die voraussichtlich in voll Bild Szenarien wie Spielen verwendet werden sollen, sollten Sie beim Erstellen der SwapChain die Angabe von [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) in [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="823dc-237">For apps that consume HDR10-encoded content, such as media players, or apps that are expected to be used mainly in fullscreen scenarios such as games, when creating your swap chain you should consider specifying [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) in [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="823dc-238">Standardmäßig wird dies als Verwendung des sRGB-Farbraum behandelt. Daher müssen Sie [**IDXGISwapChain3:: SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)explizit aufzurufen und als Farbraum [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)(auch als HDR10/BT. 2100 bezeichnet) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="823dc-238">By default, this is treated as using the sRGB color space; therefore, you must explicitly call [**IDXGISwapChain3::SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1), and set as your color space [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), also known as HDR10/BT.2100.</span></span>

<span data-ttu-id="823dc-239">Diese Kombination hat strengere Einschränkungen als FP16.</span><span class="sxs-lookup"><span data-stu-id="823dc-239">This combination has more stringent restrictions than FP16.</span></span> <span data-ttu-id="823dc-240">Dies kann nur mit Direct3D 11 oder Direct3D 12 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="823dc-240">You can use this only with Direct3D 11 or Direct3D 12.</span></span> <span data-ttu-id="823dc-241">Außerdem weist UINT10/HDR10 Einschränkungen als zwischen Format auf, da die St. 2084 EotF ("Gamma"-Funktion) verwendet wird, die sehr nicht linear ist und als Wire-Format optimiert ist, und da Sie nur 2 Bits von Alpha bietet.</span><span class="sxs-lookup"><span data-stu-id="823dc-241">In addition, UINT10/HDR10 has limitations as an intermediate format because it uses the ST.2084 EOTF ("gamma" function), which is highly nonlinear, and optimized as a wire format, and because it offers only 2 bits of alpha.</span></span>

<span data-ttu-id="823dc-242">Diese Kombination kann jedoch leistungsstarke Leistungsoptimierungen bieten, wenn Sie in der endgültigen Ausgabe Ihrer APP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="823dc-242">However, this combination can offer powerful performance optimizations when used in your app's final output.</span></span> <span data-ttu-id="823dc-243">Dabei werden die gleichen 32 Bits pro Pixel wie herkömmliche Uint8-SZR-Pixel Formate verwendet.</span><span class="sxs-lookup"><span data-stu-id="823dc-243">It consumes the same 32 bits per pixel as traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="823dc-244">Außerdem kann das Betriebssystem in bestimmten Vollbild-Szenarios die Leistung optimieren, indem es die HDR10-Oberfläche direkt scannt.</span><span class="sxs-lookup"><span data-stu-id="823dc-244">In addition, in certain fullscreen scenarios, the OS can optimize performance by directly scanning out the HDR10 surface.</span></span>

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a><span data-ttu-id="823dc-245">Verwenden einer erweiterten Farb Austausch Kette, wenn sich die Anzeige im SDR-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="823dc-245">Using an advanced color swap chain when the display is in SDR mode</span></span>

<span data-ttu-id="823dc-246">Sie können eine erweiterte Farb Austausch Kette auch dann verwenden, wenn die Anzeige einige oder alle der erweiterten Farbfunktionen, die ihr Inhalt erfordert, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="823dc-246">You can use an advanced color swap chain even if the display doesn't support some or all of the advanced color capabilities your content requires.</span></span> <span data-ttu-id="823dc-247">In diesen Fällen konvertiert der Desktopfenster-Manager (DWM) ihre Inhalte so, dass Sie den Funktionen der Anzeige angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="823dc-247">In those cases, the Desktop Window Manager (DWM) will downconvert your content to fit the display's capabilities.</span></span> <span data-ttu-id="823dc-248">In Windows 10, Version 1903 und höher, wird ein numerisches Abschneiden durchgeführt. Wenn Sie z. b. eine FP16 ScRGB-Swap-Kette renderingkette, wird alles außerhalb des numerischen Bereichs [0, 1] abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="823dc-248">In Windows 10, version 1903, and later, it will perform numeric clipping; for example, if you render to an FP16 scRGB swap chain, then everything outside of the [0, 1] numeric range is clipped.</span></span>

<span data-ttu-id="823dc-249">Dieses downkonvertierungsverhalten tritt auch auf, wenn das App-Fenster zwei oder mehr anzeigen mit unterschiedlichen erweiterten Farbfunktionen überspannt.</span><span class="sxs-lookup"><span data-stu-id="823dc-249">This downconversion behavior will also occur if your app window is straddling two or more displays with differing advanced color capabilities.</span></span> <span data-ttu-id="823dc-250">**Advancedcolorinfo** und **IDXGIOutput6** werden abstrahiert, um nur die Merkmale der Haupt Anzeige zu melden (definiert als die Anzeige, die den Mittelpunkt des Fensters enthält).</span><span class="sxs-lookup"><span data-stu-id="823dc-250">**AdvancedColorInfo** and **IDXGIOutput6** are abstracted to report only the "main" display's characteristics (defined as the display containing the center of the window).</span></span>

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a><span data-ttu-id="823dc-251">Ordnungsgemäße Rendering von "SDR Content" mit der SZR-Referenz</span><span class="sxs-lookup"><span data-stu-id="823dc-251">Correctly render SDR content with SDR reference white level</span></span>

<span data-ttu-id="823dc-252">In vielen Szenarios möchte Ihre APP sowohl den SZR-als auch den HDR-Inhalt darstellen. beispielsweise das Rendern von Untertiteln oder Transport Steuerelementen über das HDR-Video oder die Benutzeroberfläche in eine Spielszene.</span><span class="sxs-lookup"><span data-stu-id="823dc-252">In many scenarios, your app will want to render both SDR and HDR content; for example, rendering subtitles or transport controls over HDR video, or UI into a game scene.</span></span> <span data-ttu-id="823dc-253">Es ist wichtig, das Konzept der *SZR-Referenz-weißen Ebene* zu verstehen, um sicherzustellen, dass Ihr SZR-Inhalt in einer HDR-Anzeige korrekt aussieht.</span><span class="sxs-lookup"><span data-stu-id="823dc-253">It is important to understand the concept of *SDR reference white level* to ensure that your SDR content looks correct on an HDR display.</span></span>

<span data-ttu-id="823dc-254">Der HDR-Inhalt wird von Windows als _Szenen bezogen_ behandelt, was bedeutet, dass ein bestimmter Farbwert auf einer bestimmten Leuchtkraft Ebene angezeigt werden soll. beispielsweise codieren sowohl ScRGB (1,0, 1,0, 1,0) als auch HDR10 (497, 497, 497) genau D65 White bei 80 Nits-Beleuchtung.</span><span class="sxs-lookup"><span data-stu-id="823dc-254">Windows treats HDR content as _scene-referred_, meaning that a particular color value should be displayed at a specific luminance level; for example, scRGB (1.0, 1.0, 1.0) and HDR10 (497, 497, 497) both encode exactly D65 white at 80 nits luminance.</span></span> <span data-ttu-id="823dc-255">In der Zwischenzeit wurde in der Regel der _compilerinhalt ausgegeben_ (oder auf den Display verwiesen), was bedeutet, dass seine Leuchtkraft dem Benutzer oder dem Gerät überlassen wird. beispielsweise codiert sRGB (1,0, 1,0, 1,0) D65 White wie in den HDR-Beispielen, aber mit der maximalen Helligkeit, für die die Anzeige konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="823dc-255">Meanwhile, SDR content traditionally has been _output-referred_ (or display-referred), meaning that its luminance is left up to the user or the device; for example sRGB (1.0, 1.0, 1.0) encodes D65 white as in the HDR examples, but at whatever maximum luminance the display is configured for.</span></span> <span data-ttu-id="823dc-256">Mithilfe von Windows kann der Benutzer die Whitelist für den _SZR-Verweis_ auf seine bevorzugte Einstellung festlegen. Dies ist die Leuchtkraft, mit der Windows sRGB (1,0, 1,0, 1,0) in Rendering wird.</span><span class="sxs-lookup"><span data-stu-id="823dc-256">Windows allows the user to adjust the _SDR reference white level_ to their preference; this is the luminance that Windows will render sRGB (1.0, 1.0, 1.0) at.</span></span> <span data-ttu-id="823dc-257">Auf Desktop-HDR-Monitoren werden SZR-Referenz-White Levels in der Regel auf etwa 200 nits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="823dc-257">On desktop HDR monitors, SDR reference white levels are typically set to around 200 nits.</span></span>

> [!Note]
> <span data-ttu-id="823dc-258">In einer Anzeige, die ein Helligkeits Steuerelement unterstützt, wie z. b. auf einem Laptop, passt Windows auch die Leuchtkraft von HDR (Szenen bezogen) an, die der gewünschten Helligkeits Ebene des Benutzers entsprechen, aber dies ist für die APP nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="823dc-258">On a display that supports a brightness control, such as on a laptop, Windows will also adjust the luminance of HDR (scene-referred) content to match the user's desired brightness level, but this is invisible to the app.</span></span> <span data-ttu-id="823dc-259">Wenn Sie nicht versuchen, eine bitgenaue Reproduktion des HDR-Signals zu gewährleisten, können Sie dies im allgemeinen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="823dc-259">Unless you're trying to guarantee bit-accurate reproduction of the HDR signal, you can generally ignore this.</span></span>

<span data-ttu-id="823dc-260">Wenn Ihre APP immer SZR und HDR zum Trennen der Oberflächen rendert und auf der Betriebssystem Komposition basiert, führt Windows automatisch die richtige Anpassung durch, um die e/a-Inhalte auf die gewünschte weiße Ebene zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="823dc-260">If your app always renders SDR and HDR to separate surfaces, and relies on OS composition, then Windows will automatically perform the correct adjustment to boost SDR content to the desired white level.</span></span> <span data-ttu-id="823dc-261">Wenn Ihre APP z. b. XAML verwendet und den HDR-Inhalt in einem eigenen " **Swap-chainpanel**" rendert.</span><span class="sxs-lookup"><span data-stu-id="823dc-261">For example, if your app uses XAML and renders HDR content to its own **SwapChainPanel**.</span></span>

<span data-ttu-id="823dc-262">Wenn Ihre APP jedoch eine eigene Komposition von SDR-und HDR-Inhalten in einer einzigen Oberfläche ausführt, sind Sie dafür verantwortlich, die positiv Anpassung der SZR-Referenz auf der whitelinbene auszuführen.</span><span class="sxs-lookup"><span data-stu-id="823dc-262">However, if your app performs its own composition of SDR and HDR content into a single surface, then you're responsible for performing the SDR reference white level adjustment yourself.</span></span> <span data-ttu-id="823dc-263">Andernfalls erscheint der Inhalt der SDR-Inhalte möglicherweise zu schlecht, wenn Sie typische Desktop Anzeige Bedingungen annehmen</span><span class="sxs-lookup"><span data-stu-id="823dc-263">Otherwise the SDR content might appear too dim assuming typical desktop viewing conditions.</span></span> <span data-ttu-id="823dc-264">Zuerst müssen Sie die aktuelle SZR-Referenz-White-Ebene abrufen und dann die Farbwerte aller von Ihnen renderenden SZR-Inhalte anpassen.</span><span class="sxs-lookup"><span data-stu-id="823dc-264">First, you must obtain the current SDR reference white level, and then you must adjust the color values of any SDR content you're rendering.</span></span>

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a><span data-ttu-id="823dc-265">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="823dc-265">Step 1.</span></span> <span data-ttu-id="823dc-266">Abrufen der aktuellen SZR-Referenz-weißen Ebene</span><span class="sxs-lookup"><span data-stu-id="823dc-266">Obtain the current SDR reference white level</span></span>

<span data-ttu-id="823dc-267">Derzeit können nur UWP-Apps die aktuelle SZR-Referenz-weißen Ebene über [**advancedcolorinfo. sdrwhitelevelinnits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits)abrufen.</span><span class="sxs-lookup"><span data-stu-id="823dc-267">Currently, only UWP apps can obtain the current SDR reference white level via [**AdvancedColorInfo.SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits).</span></span> <span data-ttu-id="823dc-268">Diese API erfordert ein [**corewindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="823dc-268">This API requires a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

### <a name="step-2-adjust-color-values-of-sdr-content"></a><span data-ttu-id="823dc-269">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="823dc-269">Step 2.</span></span> <span data-ttu-id="823dc-270">Anpassen von Farbwerten von "SDR Content"</span><span class="sxs-lookup"><span data-stu-id="823dc-270">Adjust color values of SDR content</span></span>

<span data-ttu-id="823dc-271">Windows definiert den nominalen bzw. den Standard Verweis auf die weiße Ebene bei 80 Nits. Wenn Sie also eine standardmäßige sRGB-(1,0, 1,0, 1,0) weiß in einer FP16-SwapChain gerenden, wird Sie bei der "80 Nits"-Beleuchtung reproduziert.</span><span class="sxs-lookup"><span data-stu-id="823dc-271">Windows defines the nominal, or default, reference white level at 80 nits; therefore if you were to render a standard sRGB (1.0, 1.0, 1.0) white to an FP16 swap chain, it would be reproduced at 80 nits luminance.</span></span> <span data-ttu-id="823dc-272">Um die tatsächliche benutzerdefinierte Verweis-weißen Ebene abzugleichen, müssen Sie den compilerinhalt von 80 Nits an die Ebene anpassen, die über **advancedcolorinfo. sdrwhitelevelinnits** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="823dc-272">In order to match the actual user-defined reference white level, you must adjust SDR content from 80 nits to the level specified via **AdvancedColorInfo.SdrWhiteLevelInNits**.</span></span>

<span data-ttu-id="823dc-273">Wenn Sie mithilfe von FP16 und ScRGB oder mit einem beliebigen Farbraum, der lineare (1,0) Gamma verwendet, gerendert werden, können Sie einfach den Wert von "SDR" durch _advancedcolorinfo. sdrwhitelevelinnits_  /  _80_ multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="823dc-273">If you're rendering using FP16 and scRGB, or any color space that uses linear (1.0) gamma, then you can simply multiply the SDR color value by _AdvancedColorInfo.SdrWhiteLevelInNits_ / _80_.</span></span> <span data-ttu-id="823dc-274">Wenn Sie Direct2D verwenden, gibt es eine vordefinierte Konstante [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f)mit einem Wert von 80.</span><span class="sxs-lookup"><span data-stu-id="823dc-274">If you're using Direct2D, there is a predefined constant [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), which has a value of 80.</span></span>

```cpp
D2D1_VECTOR_4F inputColor; // Input SDR color value.
D2D1_VECTOR_4F outputColor; // Output color adjusted for SDR white level.
auto acInfo; // AdvancedColorInfo

float sdrAdjust = acInfo->SdrWhiteLevelInNits / D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL;

// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
outputColor.r = inputColor.r * sdrAdjust; // Assumes linear gamma color values.
outputColor.g = inputColor.g * sdrAdjust;
outputColor.b = inputColor.b * sdrAdjust;
outputColor.a = inputColor.a;
```

<span data-ttu-id="823dc-275">Wenn Sie mit einem nichtlinearen Gamma-Farbraum wie HDR10 rendern, ist die Durchführung der Farb verarbeistung der SZR-Ebene komplexer. Wenn Sie einen eigenen Pixelshader schreiben, sollten Sie in Erwägung gezogen werden, die Anpassung in lineare Gamma vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="823dc-275">If you're rendering using a nonlinear gamma color space such as HDR10, then performing SDR white level adjustment is more complex; if you're writing your own pixel shader you should consider converting into linear gamma to apply the adjustment.</span></span>

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a><span data-ttu-id="823dc-276">Anpassen von HDR-Inhalten an die Anzeigefunktionen mithilfe von Tonemapping</span><span class="sxs-lookup"><span data-stu-id="823dc-276">Adapt HDR content to the display's capabilities using tonemapping</span></span>

<span data-ttu-id="823dc-277">Die Farbe "HDR" und "Advanced" unterscheiden sich in Bezug auf ihre Funktionen stark.</span><span class="sxs-lookup"><span data-stu-id="823dc-277">HDR and advanced color displays vary greatly in terms of their capabilities.</span></span> <span data-ttu-id="823dc-278">Beispielsweise die minimale und die maximale Leuchtkraft und die Farbpalette, die Sie reproduzieren können.</span><span class="sxs-lookup"><span data-stu-id="823dc-278">For example, the minimum and maximum luminance and the color gamut they are capable of reproducing.</span></span> <span data-ttu-id="823dc-279">In vielen Fällen enthalten die HDR-Inhalte Farben, die die Anzeigefunktionen überschreiten.</span><span class="sxs-lookup"><span data-stu-id="823dc-279">In many cases, your HDR content will contain colors that exceed the display's capabilities.</span></span> <span data-ttu-id="823dc-280">Um die beste Bildqualität zu erzielen, ist es wichtig, dass Sie HDR Tonemapping durchführen, wobei der Bereich der Farben im Grunde an die Anzeige angepasst wird, während die visuelle Absicht der Inhalte am besten gewahrt bleibt.</span><span class="sxs-lookup"><span data-stu-id="823dc-280">For the best image quality it is important for you to perform HDR tonemapping, essentially compressing the range of colors to fit the display while best preserving the visual intent of the content.</span></span>

<span data-ttu-id="823dc-281">Der wichtigste einzige Parameter für die Anpassung ist die maximale Helligkeit, auch bekannt als maxcll (Content Light Level). komplexere Tonmapper passen auch min. Leuchtkraft (mincll) und/oder Farb Replikate an.</span><span class="sxs-lookup"><span data-stu-id="823dc-281">The most important single parameter to adapt for is max luminance, also known as MaxCLL (content light level); more sophisticated tonemappers will also adapt min luminance (MinCLL) and/or color primaries.</span></span>

### <a name="step-1-get-the-displays-color-volume-capabilities"></a><span data-ttu-id="823dc-282">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="823dc-282">Step 1.</span></span> <span data-ttu-id="823dc-283">Hiermit werden die Farbvolumen Funktionen der Anzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="823dc-283">Get the display's color volume capabilities</span></span>

#### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="823dc-284">Universelle Windows-Plattform-Apps (UWP)</span><span class="sxs-lookup"><span data-stu-id="823dc-284">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="823dc-285">Verwenden Sie [**advancedcolorinfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) , um das farbvolume der Anzeige zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="823dc-285">Use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get the display's color volume.</span></span>

#### <a name="win32-desktop-directx-apps"></a><span data-ttu-id="823dc-286">Win32-Apps (Desktop)</span><span class="sxs-lookup"><span data-stu-id="823dc-286">Win32 (desktop) DirectX apps</span></span>

<span data-ttu-id="823dc-287">Verwenden Sie [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) , um das farbvolume der Anzeige zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="823dc-287">Use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get the display's color volume.</span></span>

### <a name="step-2-get-the-contents-color-volume-information"></a><span data-ttu-id="823dc-288">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="823dc-288">Step 2.</span></span> <span data-ttu-id="823dc-289">Die farbvolumeinformationen des Inhalts erhalten.</span><span class="sxs-lookup"><span data-stu-id="823dc-289">Get the content's color volume information</span></span>

<span data-ttu-id="823dc-290">Abhängig davon, woher der HDR-Inhalt stammt, gibt es mehrere Möglichkeiten, seine Beleuchtungs-und Farb Spielinformationen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="823dc-290">Depending on where your HDR content came from, there are multiple potential ways to determine its luminance and color gamut information.</span></span> <span data-ttu-id="823dc-291">Bestimmte HDR-Video-und Bilddateien enthalten SMPTE St. 2086-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="823dc-291">Certain HDR video and image files contain SMPTE ST.2086 metadata.</span></span> <span data-ttu-id="823dc-292">Wenn Ihr Inhalt dynamisch gerendert wurde, können Sie möglicherweise szeneninformationen aus den internen renderingstufen extrahieren, z. b. die hellste helle Quelle in einer Szene.</span><span class="sxs-lookup"><span data-stu-id="823dc-292">If your content was rendered dynamically, then you may be able to extract scene information from the internal rendering stages, for example the brightest light source in a scene.</span></span>

<span data-ttu-id="823dc-293">Eine allgemeinere, aber Rechen aufwändige Lösung besteht darin, ein Histogramm oder einen anderen Analyse Durchlauf für den gerenderten Frame auszuführen.</span><span class="sxs-lookup"><span data-stu-id="823dc-293">A more general but computationally expensive solution is to run a histogram or other analysis pass on the rendered frame.</span></span> <span data-ttu-id="823dc-294">Das [Direct2D Advanced Color Images SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) veranschaulicht, wie dies mithilfe von Direct2D durchzuführen ist. die relevantesten Code Ausschnitte sind unten aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="823dc-294">The [Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) demonstrates how to do this using Direct2D; the most relevant code snippets are included below:</span></span>

```cpp
// Perform histogram pipeline setup; this should occur as part of image resource creation.
// Histogram results in no visual output but is used to calculate HDR metadata for the image.
void D2DAdvancedColorImagesRenderer::CreateHistogramResources()
{
    auto context = m_deviceResources->GetD2DDeviceContext();

    // We need to preprocess the image data before running the histogram.
    // 1. Spatial downscale to reduce the amount of processing needed.
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1Scale, &m_histogramPrescale)
        );

    DX::ThrowIfFailed(
        m_histogramPrescale->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(0.5f, 0.5f))
        );

    // The right place to compute HDR metadata is after color management to the
    // image's native colorspace but before any tonemapping or adjustments for the display.
    m_histogramPrescale->SetInputEffect(0, m_colorManagementEffect.Get());

    // 2. Convert scRGB data into luminance (nits).
    // 3. Normalize color values. Histogram operates on [0-1] numeric range,
    //    while FP16 can go up to 65504 (5+ million nits).
    // Both steps are performed in the same color matrix.
    ComPtr<ID2D1Effect> histogramMatrix;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1ColorMatrix, &histogramMatrix)
        );

    histogramMatrix->SetInputEffect(0, m_histogramPrescale.Get());

    float scale = sc_histMaxNits / sc_nominalRefWhite;

    D2D1_MATRIX_5X4_F rgbtoYnorm = D2D1::Matrix5x4F(
        0.2126f / scale, 0, 0, 0,
        0.7152f / scale, 0, 0, 0,
        0.0722f / scale, 0, 0, 0,
        0              , 0, 0, 1,
        0              , 0, 0, 0);
    // 1st column: [R] output, contains normalized Y (CIEXYZ).
    // 2nd column: [G] output, unused.
    // 3rd column: [B] output, unused.
    // 4th column: [A] output, alpha passthrough.
    // We explicitly calculate Y; this deviates from the CEA 861.3 definition of MaxCLL
    // which approximates luminance with max(R, G, B).

    DX::ThrowIfFailed(histogramMatrix->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, rgbtoYnorm));

    // 4. Apply a gamma to allocate more histogram bins to lower luminance levels.
    ComPtr<ID2D1Effect> histogramGamma;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1GammaTransfer, &histogramGamma)
        );

    histogramGamma->SetInputEffect(0, histogramMatrix.Get());

    // Gamma function offers an acceptable tradeoff between simplicity and efficient bin allocation.
    // A more sophisticated pipeline would use a more perceptually linear function than gamma.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, sc_histGamma));
    // All other channels are passthrough.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, TRUE));

    // 5. Finally, the histogram itself.
    HRESULT hr = context->CreateEffect(CLSID_D2D1Histogram, &m_histogramEffect);
    
    if (hr == D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES)
    {
        // The GPU doesn't support compute shaders and we can't run histogram on it.
        m_isComputeSupported = false;
    }
    else
    {
        DX::ThrowIfFailed(hr);
        m_isComputeSupported = true;

        DX::ThrowIfFailed(m_histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, sc_histNumBins));

        m_histogramEffect->SetInputEffect(0, histogramGamma.Get());
    }
}

// Uses a histogram to compute a modified version of MaxCLL (ST.2086 max content light level).
// Performs Begin/EndDraw on the D2D context.
void D2DAdvancedColorImagesRenderer::ComputeHdrMetadata()
{
    // Initialize with a sentinel value.
    m_maxCLL = -1.0f;

    // MaxCLL is not meaningful for SDR or WCG images.
    if ((!m_isComputeSupported) ||
        (m_imageInfo.imageKind != AdvancedColorKind::HighDynamicRange))
    {
        return;
    }

    // MaxCLL is nominally calculated for the single brightest pixel in a frame.
    // But we take a slightly more conservative definition that takes the 99.99th percentile
    // to account for extreme outliers in the image.
    float maxCLLPercent = 0.9999f;

    auto ctx = m_deviceResources->GetD2DDeviceContext();

    ctx->BeginDraw();

    ctx->DrawImage(m_histogramEffect.Get());

    // We ignore D2DERR_RECREATE_TARGET here. This error indicates that the device
    // is lost. It will be handled during the next call to Present.
    HRESULT hr = ctx->EndDraw();
    if (hr != D2DERR_RECREATE_TARGET)
    {
        DX::ThrowIfFailed(hr);
    }

    float *histogramData = new float[sc_histNumBins];
    DX::ThrowIfFailed(
        m_histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT,
            reinterpret_cast<BYTE*>(histogramData),
            sc_histNumBins * sizeof(float)
            )
        );

    unsigned int maxCLLbin = 0;
    float runningSum = 0.0f; // Cumulative sum of values in histogram is 1.0.
    for (int i = sc_histNumBins - 1; i >= 0; i--)
    {
        runningSum += histogramData[i];
        maxCLLbin = i;

        if (runningSum >= 1.0f - maxCLLPercent)
        {
            break;
        }
    }

    float binNorm = static_cast<float>(maxCLLbin) / static_cast<float>(sc_histNumBins);
    m_maxCLL = powf(binNorm, 1 / sc_histGamma) * sc_histMaxNits;

    // Some drivers have a bug where histogram will always return 0. Treat this as unknown.
    m_maxCLL = (m_maxCLL == 0.0f) ? -1.0f : m_maxCLL;
}
```

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a><span data-ttu-id="823dc-295">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="823dc-295">Step 3.</span></span> <span data-ttu-id="823dc-296">Ausführen des Vorgangs "HDR Tonemapping"</span><span class="sxs-lookup"><span data-stu-id="823dc-296">Perform the HDR tonemapping operation</span></span>

<span data-ttu-id="823dc-297">Tonemapping ist naturgemäß ein verlustfreier Prozess und kann für eine Reihe von perzeptive oder zielmetriken optimiert werden, sodass es keinen Standard Algorithmus gibt.</span><span class="sxs-lookup"><span data-stu-id="823dc-297">Tonemapping is inherently a lossy process, and can be optimized for a number of perceptual or objective metrics, so there is no one standard algorithm.</span></span> <span data-ttu-id="823dc-298">Windows bietet einen integrierten [HDR Tonemapper-Effekt](../direct2d/hdr-tone-map-effect.md) als Teil von Direct2D und in der Media Foundation HDR-Videowiedergabe Pipeline.</span><span class="sxs-lookup"><span data-stu-id="823dc-298">Windows provides a built-in [HDR tonemapper effect](../direct2d/hdr-tone-map-effect.md) as part of Direct2D as well as in the Media Foundation HDR video playback pipeline.</span></span> <span data-ttu-id="823dc-299">Einige andere häufig verwendete Algorithmen sind ACEs filmic, Reinhard und ITU-R BT. 2390-3 EETF (Electric-Electrical Transfer Function).</span><span class="sxs-lookup"><span data-stu-id="823dc-299">Some other commonly used algorithms include ACES Filmic, Reinhard, and ITU-R BT.2390-3 EETF (electrical-electrical transfer function).</span></span>

<span data-ttu-id="823dc-300">Unten ist ein vereinfachter Reinhard Tonemapper-Operator angegeben.</span><span class="sxs-lookup"><span data-stu-id="823dc-300">A simplified Reinhard tonemapper operator is shown below.</span></span>

```cpp
// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
D2D1_VECTOR_4F simpleReinhardTonemapper(
    float inputMax, // Content's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    float outputMax, // Display's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    D2D1_VECTOR_4F input // scRGB color.
)
{
    D2D1_VECTOR_4F output = input;

    // Vanilla Reinhard normalizes color values to [0, 1].
    // This modification scales to the luminance range of the display.
    output.r /= inputMax;
    output.g /= inputMax;
    output.b /= inputMax;

    output.r = (output.r / 1 + output.r);
    output.g = (output.g / 1 + output.g);
    output.b = (output.b / 1 + output.b);

    output.r *= outputMax;
    output.g *= outputMax;
    output.b *= outputMax;

    return output;
}
```

## <a name="capturing-hdr-and-wcg-content"></a><span data-ttu-id="823dc-301">Erfassen von HDR-und WCG-Inhalten</span><span class="sxs-lookup"><span data-stu-id="823dc-301">Capturing HDR and WCG content</span></span>

<span data-ttu-id="823dc-302">APIs, die die Angabe von Pixel Formaten unterstützen, wie z. b. die im [**Windows. Graphics. Capture**](/uwp/api/windows.graphics.capture) -Namespace und die [**IDXGIOutput5::D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) -Methode, bieten die Möglichkeit, HDR-und WCG-Inhalte zu erfassen, ohne Pixel Informationen zu verlieren.</span><span class="sxs-lookup"><span data-stu-id="823dc-302">APIs that support specifying pixel formats, such as those in the [**Windows.Graphics.Capture**](/uwp/api/windows.graphics.capture) namespace, and the [**IDXGIOutput5::DuplicateOutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) method, provide the capability to capture HDR and WCG content without losing pixel information.</span></span> <span data-ttu-id="823dc-303">Beachten Sie, dass nach dem Erwerb von Inhalts Frames zusätzliche Verarbeitungsschritte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="823dc-303">Note that after acquiring content frames, additional processing is required.</span></span> <span data-ttu-id="823dc-304">Beispielsweise die HDR-zu-SZR-Zuordnungs Zuordnung (z. b. "htmscreencopy" für die Internet Freigabe) und die Speicherung von Inhalten mit dem richtigen Format (z. b. JPEG XR).</span><span class="sxs-lookup"><span data-stu-id="823dc-304">For example, HDR-to-SDR tone mapping (for example, SDR screenshot copy for Internet sharing) and content saving with proper format (for example, JPEG XR).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="823dc-305">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="823dc-305">Additional resources</span></span>

* <span data-ttu-id="823dc-306">*Verwenden des HDR-Rendering mit dem DirectX-Toolkit* für [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span><span class="sxs-lookup"><span data-stu-id="823dc-306">*Using HDR Rendering with the DirectX Tool Kit* for [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering) / [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span></span> <span data-ttu-id="823dc-307">Exemplarische Vorgehensweise zum Hinzufügen von HDR-Unterstützung zu einer DirectX-App mithilfe des DirectX-Toolkits (directxtk).</span><span class="sxs-lookup"><span data-stu-id="823dc-307">Walkthrough of how to add HDR support to a DirectX app using the DirectX Tool Kit (DirectXTK).</span></span>
* <span data-ttu-id="823dc-308">[Direct2D Advanced Color Images SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span><span class="sxs-lookup"><span data-stu-id="823dc-308">[Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span></span> <span data-ttu-id="823dc-309">UWP SDK-Beispiel, das einen erweiterten Farb abhängigen HDR-und WCG-Bild-Viewer mit Direct2D implementiert.</span><span class="sxs-lookup"><span data-stu-id="823dc-309">UWP SDK sample implementing an advanced color-aware HDR and WCG image viewer using Direct2D.</span></span> <span data-ttu-id="823dc-310">Veranschaulicht die vollständige Palette der bewährten Methoden für UWP-apps, einschließlich der Reaktion auf Änderungen der Anzeigefunktionen und der Anpassung für die e/a-weißen Ebene.</span><span class="sxs-lookup"><span data-stu-id="823dc-310">Demonstrates the full range of best practices for UWP apps, including responding to display capability changes and adjusting for SDR white level.</span></span>
* <span data-ttu-id="823dc-311">[Direct3D 12 HDR Desktop-Beispiel](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="823dc-311">[Direct3D 12 HDR desktop sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span> <span data-ttu-id="823dc-312">Desktop SDK-Beispiel, das eine grundlegende Direct3D 12 HDR-Szene implementiert.</span><span class="sxs-lookup"><span data-stu-id="823dc-312">Desktop SDK sample implementing a basic Direct3D 12 HDR scene.</span></span>
* <span data-ttu-id="823dc-313">[Direct3D 12 HDR UWP-Beispiel](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="823dc-313">[Direct3D 12 HDR UWP sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span></span> <span data-ttu-id="823dc-314">UWP-Entsprechung des obigen Beispiels.</span><span class="sxs-lookup"><span data-stu-id="823dc-314">UWP equivalent of the above sample.</span></span>
* <span data-ttu-id="823dc-315">[Xbox ATG simplehdr-PC-Beispiel](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span><span class="sxs-lookup"><span data-stu-id="823dc-315">[Xbox ATG SimpleHDR PC sample](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span></span> <span data-ttu-id="823dc-316">Desktop SDK-Beispiel, das eine grundlegende Direct3D 11 HDR-Szene implementiert.</span><span class="sxs-lookup"><span data-stu-id="823dc-316">Desktop SDK sample implementing a basic Direct3D 11 HDR scene.</span></span>
