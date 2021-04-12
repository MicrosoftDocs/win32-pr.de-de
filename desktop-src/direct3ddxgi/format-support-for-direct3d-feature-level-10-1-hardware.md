---
description: In diesem Abschnitt werden die Formate ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die auf Direct3D Feature Level 10,1-Hardware unterstützt werden.
ms.assetid: 2C7E16D7-EEF0-4EA7-A819-5274C9105F68
title: Formatunterstützung für Direct3D 10.1-Hardware auf Featureebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edb5c81ef0a99bc14031a9a7a505736e91e13d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481294"
---
# <a name="format-support-for-direct3d-feature-level-101-hardware"></a><span data-ttu-id="090f0-103">Formatunterstützung für Direct3D 10.1-Hardware auf Featureebene</span><span class="sxs-lookup"><span data-stu-id="090f0-103">Format support for Direct3D Feature Level 10.1 hardware</span></span>

<span data-ttu-id="090f0-104">In diesem Abschnitt werden die Formate ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die auf Direct3D Feature Level 10,1-Hardware unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="090f0-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.1 hardware.</span></span>

<span data-ttu-id="090f0-105">Die Tabelle enthält eine Zusammenfassung der Featureunterstützung, die den folgenden Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="090f0-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="090f0-106">Symbol</span><span class="sxs-lookup"><span data-stu-id="090f0-106">Symbol</span></span>                            | <span data-ttu-id="090f0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="090f0-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="090f0-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="090f0-108">_ *-*\*</span></span>                             | <span data-ttu-id="090f0-109">Nicht zulässig oder nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="090f0-109">Disallowed or not available.</span></span>                                                  |
| ![Erforderlich](images/letter-r.jpg)  | <span data-ttu-id="090f0-111">Hardware Unterstützung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="090f0-111">Hardware support is required.</span></span>                                                 |
| ![Optional](images/letter-o.jpg)  | <span data-ttu-id="090f0-113">Hardwareunterstützung optional, das Format ist möglicherweise Hardware beschleunigt.</span><span class="sxs-lookup"><span data-stu-id="090f0-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![lässe](images/letter-d.jpg) | <span data-ttu-id="090f0-115">Erforderlich, wenn eine zugehörige optionale Funktion unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="090f0-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="090f0-116">Dieses Thema enthält einen Abschnitt Pro Format.</span><span class="sxs-lookup"><span data-stu-id="090f0-116">This topic contains a section per format.</span></span> <span data-ttu-id="090f0-117">Ein Format *Ziel* (die Tabellen enthalten eine Zeile pro Ziel) kann ein Ressourcentyp, eine intrinsische HLSL-Funktion oder eine bestimmte Funktionalität sein, die von einem bestimmten Format abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="090f0-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="090f0-118">Informationen zur programmgesteuerten Überprüfung der Formatunterstützung in D3D11 und D3D12 finden Sie unter über [Prüfen der Unterstützung von Hardwarefunktionen](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="090f0-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="090f0-119">Die Zahlen der Formate sind größtenteils, aber nicht alle in aufsteigender numerischer Reihenfolge, dass einige nicht in &mdash; numerischer Reihenfolge sind und neben anderen relevanten Formaten aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="090f0-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="090f0-120">Beachten Sie auch, dass *typlose* in einem Format Namen *teilweise* typisiert und nicht streng typlos sein kann (Weitere Informationen finden Sie im Abschnitt " [Format Notizen](#format-notes) " am Ende des Themas).</span><span class="sxs-lookup"><span data-stu-id="090f0-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="090f0-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="090f0-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="090f0-122">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-122">Target</span></span> | <span data-ttu-id="090f0-123">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-123">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-124">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-125">0</span><span class="sxs-lookup"><span data-stu-id="090f0-125">0</span></span> |
| <span data-ttu-id="090f0-126">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-126">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-128">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-130">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-131">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-132">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-133">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-134">Texture2D</span></span> | \- |
| <span data-ttu-id="090f0-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-135">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-136">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-137">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-137">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-138">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-139">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-140">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-141">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-142">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-143">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-143">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-144">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-146">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-147">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-148">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-149">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-150">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-151">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-152">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-153">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-154">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-155">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-157">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-158">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-159">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-160">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-160">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-162">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-163">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-164">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-165">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-166">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-167">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-168">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-169">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-170">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-171">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-172">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-173">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="090f0-174">DXGI_FORMAT_R32G32B32A32 \_ Typen losen<sup>PCs</sup> (1)</span><span class="sxs-lookup"><span data-stu-id="090f0-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="090f0-175">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-175">Target</span></span> | <span data-ttu-id="090f0-176">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-176">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-177">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-178">128</span><span class="sxs-lookup"><span data-stu-id="090f0-178">128</span></span> |
| <span data-ttu-id="090f0-179">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-179">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-181">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-181">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-182">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-183">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-184">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-185">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-187">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-189">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-191">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-193">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-193">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-194">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-195">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-196">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-197">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-198">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-199">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-199">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-201">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-202">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-203">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-204">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-205">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-206">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-207">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-208">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-209">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-210">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-211">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-212">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-213">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-214">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-215">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-216">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-217">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-217">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-219">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-220">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-221">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-222">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-223">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-224">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-225">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-225">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-227">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-228">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-229">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-230">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-230">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-232">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="090f0-233">DXGI_FORMAT_R32G32B32A32 \_ float<sup></sup> -Zeichen (2)</span><span class="sxs-lookup"><span data-stu-id="090f0-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="090f0-234">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-234">Target</span></span> | <span data-ttu-id="090f0-235">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-235">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-236">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-237">128</span><span class="sxs-lookup"><span data-stu-id="090f0-237">128</span></span> |
| <span data-ttu-id="090f0-238">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-238">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-240">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-240">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-242">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-242">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-244">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-245">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-245">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-247">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-249">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-251">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-253">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-255">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-255">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-257">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-257">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-259">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-260">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-261">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-262">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-263">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-263">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-265">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-265">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-267">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-269">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-269">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-271">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-272">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-273">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-274">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-275">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-276">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-277">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-278">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-279">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-280">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-281">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-282">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-283">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-284">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-284">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-286">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-286">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-288">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-288">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-290">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-290">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-292">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-292">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-294">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-294">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-296">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-297">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-297">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-299">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-300">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-301">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-302">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-302">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-304">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="090f0-305">DXGI_FORMAT_R32G32B32A32 \_ uint-<sup>f</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="090f0-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="090f0-306">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-306">Target</span></span> | <span data-ttu-id="090f0-307">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-307">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-308">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-309">128</span><span class="sxs-lookup"><span data-stu-id="090f0-309">128</span></span> |
| <span data-ttu-id="090f0-310">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-310">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-312">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-312">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-314">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-314">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-316">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-317">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-317">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-319">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-321">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-323">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-325">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-327">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-327">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-329">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-330">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-331">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-332">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-333">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-334">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-334">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-336">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-337">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-337">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-339">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-340">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-340">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-342">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-343">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-344">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-345">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-346">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-347">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-348">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-349">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-350">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-351">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-352">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-353">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-354">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-354">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-356">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-356">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-358">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-358">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-360">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-360">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-362">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-363">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-363">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-365">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-366">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-366">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-368">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-369">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-370">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-371">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-371">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-373">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="090f0-374">DXGI_FORMAT_R32G32B32A32 \_ Sint<sup></sup> (4)</span><span class="sxs-lookup"><span data-stu-id="090f0-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="090f0-375">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-375">Target</span></span> | <span data-ttu-id="090f0-376">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-376">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-377">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-378">128</span><span class="sxs-lookup"><span data-stu-id="090f0-378">128</span></span> |
| <span data-ttu-id="090f0-379">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-379">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-381">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-381">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-383">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-383">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-385">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-386">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-386">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-388">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-390">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-392">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-394">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-396">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-396">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-398">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-399">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-400">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-401">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-402">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-403">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-403">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-405">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-406">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-408">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-409">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-410">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-411">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-412">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-413">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-414">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-415">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-416">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-417">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-419">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-420">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-421">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-422">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-422">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-424">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-424">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-426">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-426">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-428">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-428">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-430">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-431">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-431">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-433">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-434">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-434">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-436">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-437">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-438">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-439">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-439">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-441">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="090f0-442">DXGI_FORMAT_R32G32B32 \_ Typen losen<sup>PCs</sup> (5)</span><span class="sxs-lookup"><span data-stu-id="090f0-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="090f0-443">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-443">Target</span></span> | <span data-ttu-id="090f0-444">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-444">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-445">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-446">96</span><span class="sxs-lookup"><span data-stu-id="090f0-446">96</span></span> |
| <span data-ttu-id="090f0-447">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-447">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-449">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-449">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-450">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-451">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-452">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-453">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-455">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-457">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-459">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-461">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-461">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-462">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-463">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-464">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-465">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-466">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-467">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-467">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-469">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-471">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-472">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-473">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-474">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-475">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-476">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-477">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-478">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-479">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-480">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-482">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-483">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-484">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-485">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-485">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-487">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-488">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-489">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-490">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-491">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-492">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-493">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-493">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-495">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-496">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-497">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-498">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-499">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="090f0-500">DXGI_FORMAT_R32G32B32 \_ float<sup></sup> -Zeichen (6)</span><span class="sxs-lookup"><span data-stu-id="090f0-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="090f0-501">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-501">Target</span></span> | <span data-ttu-id="090f0-502">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-502">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-503">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-504">96</span><span class="sxs-lookup"><span data-stu-id="090f0-504">96</span></span> |
| <span data-ttu-id="090f0-505">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-505">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-507">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-507">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-509">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-509">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-511">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-512">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-512">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-514">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-516">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-518">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-520">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-522">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-522">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-524">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-524">Shader sample (any filter)</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-526">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-527">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-528">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-529">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-530">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-530">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-532">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-532">Mipmap Auto-Generation</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-534">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-536">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-536">Blendable RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="090f0-538">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-539">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-540">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-541">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-542">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-543">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-544">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-545">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-546">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-547">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-548">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-549">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-550">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-551">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-551">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-553">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-553">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="090f0-555">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-555">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="090f0-557">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-557">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-559">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-559">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-561">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-561">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-563">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-564">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-564">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-566">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-567">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-568">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-569">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-570">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="090f0-571">DXGI_FORMAT_R32G32B32 \_ uint-<sup>f</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="090f0-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="090f0-572">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-572">Target</span></span> | <span data-ttu-id="090f0-573">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-573">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-574">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-575">96</span><span class="sxs-lookup"><span data-stu-id="090f0-575">96</span></span> |
| <span data-ttu-id="090f0-576">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-576">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-578">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-578">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-580">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-580">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-582">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-583">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-583">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-585">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-587">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-589">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-591">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-593">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-593">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-595">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-596">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-597">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-598">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-599">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-600">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-600">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-602">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-603">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-603">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-605">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-606">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-606">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-608">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-609">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-610">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-611">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-612">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-613">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-614">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-615">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-616">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-617">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-618">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-619">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-620">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-620">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-622">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-622">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="090f0-624">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-624">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="090f0-626">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-626">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-628">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-629">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-629">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-631">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-632">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-632">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-634">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-635">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-636">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-637">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-638">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="090f0-639">DXGI_FORMAT_R32G32B32 \_ Sint<sup></sup> -Karten (8)</span><span class="sxs-lookup"><span data-stu-id="090f0-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="090f0-640">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-640">Target</span></span> | <span data-ttu-id="090f0-641">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-641">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-642">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-643">96</span><span class="sxs-lookup"><span data-stu-id="090f0-643">96</span></span> |
| <span data-ttu-id="090f0-644">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-644">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-646">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-646">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-648">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-648">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-650">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-651">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-651">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-653">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-655">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-657">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-659">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-661">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-661">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-663">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-664">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-665">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-666">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-667">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-668">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-668">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-670">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-671">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-671">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-673">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-674">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-675">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-676">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-677">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-678">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-679">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-680">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-681">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-682">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-684">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-685">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-686">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-687">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-687">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-689">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-689">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="090f0-691">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-691">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="090f0-693">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-693">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-695">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-696">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-696">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-698">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-699">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-699">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-701">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-702">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-703">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-704">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-705">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="090f0-706">DXGI_FORMAT_R16G16B16A16 \_ Typen losen<sup>PCs</sup> (9)</span><span class="sxs-lookup"><span data-stu-id="090f0-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="090f0-707">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-707">Target</span></span> | <span data-ttu-id="090f0-708">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-708">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-709">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-710">64</span><span class="sxs-lookup"><span data-stu-id="090f0-710">64</span></span> |
| <span data-ttu-id="090f0-711">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-711">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-713">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-713">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-714">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-715">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-716">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-717">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-719">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-721">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-723">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-725">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-725">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-726">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-727">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-728">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-729">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-730">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-731">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-731">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-733">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-734">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-735">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-736">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-737">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-738">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-739">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-740">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-741">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-742">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-743">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-744">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-745">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-746">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-747">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-748">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-749">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-749">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-751">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-752">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-753">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-754">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-755">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-756">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-757">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-757">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-759">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-760">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-761">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-762">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-762">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-764">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="090f0-765">DXGI_FORMAT_R16G16B16A16 \_ float<sup></sup> -Zeichen (10)</span><span class="sxs-lookup"><span data-stu-id="090f0-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="090f0-766">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-766">Target</span></span> | <span data-ttu-id="090f0-767">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-767">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-768">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-769">64</span><span class="sxs-lookup"><span data-stu-id="090f0-769">64</span></span> |
| <span data-ttu-id="090f0-770">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-770">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-772">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-772">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-774">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-774">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-776">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-777">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-778">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-780">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-782">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-784">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-786">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-786">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-788">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-788">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-790">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-791">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-792">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-793">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-794">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-794">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-796">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-796">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-798">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-798">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-800">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-800">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-802">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-803">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-804">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-805">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-806">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-807">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-808">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-809">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-810">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-811">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-812">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-813">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-814">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-815">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-815">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-817">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-817">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-819">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-819">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-821">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-821">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-823">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-823">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-825">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-825">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-827">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-827">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-829">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-829">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-831">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-832">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-832">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-834">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-834">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-836">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-836">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-838">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="090f0-839">DXGI_FORMAT_R16G16B16A16 \_ unorm-Datei-<sup>e</sup> /a (11)</span><span class="sxs-lookup"><span data-stu-id="090f0-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="090f0-840">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-840">Target</span></span> | <span data-ttu-id="090f0-841">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-841">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-842">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-843">64</span><span class="sxs-lookup"><span data-stu-id="090f0-843">64</span></span> |
| <span data-ttu-id="090f0-844">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-844">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-846">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-846">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-848">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-848">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-850">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-851">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-852">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-854">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-856">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-858">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-860">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-860">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-862">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-862">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-864">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-865">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-866">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-867">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-868">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-868">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-870">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-870">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-872">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-872">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-874">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-874">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-876">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-877">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-878">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-879">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-880">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-881">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-882">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-883">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-884">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-886">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-887">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-888">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-889">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-889">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-891">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-891">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-893">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-893">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-895">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-895">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-897">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-897">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-899">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-899">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-901">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-902">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-902">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-904">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-905">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-906">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-907">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-907">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-909">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="090f0-910">DXGI_FORMAT_R16G16B16A16 \_ uint-<sup>f</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="090f0-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="090f0-911">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-911">Target</span></span> | <span data-ttu-id="090f0-912">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-912">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-913">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-914">64</span><span class="sxs-lookup"><span data-stu-id="090f0-914">64</span></span> |
| <span data-ttu-id="090f0-915">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-915">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-917">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-917">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-919">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-919">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-921">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-922">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-923">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-925">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-927">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-929">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-931">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-931">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-933">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-934">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-935">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-936">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-937">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-938">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-938">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-940">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-941">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-941">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-943">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-944">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-944">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-946">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-947">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-948">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-949">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-950">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-951">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-952">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-953">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-954">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-955">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-956">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-957">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-958">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-958">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-960">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-960">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-962">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-962">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-964">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-964">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-966">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-967">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-967">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-969">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-970">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-970">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-972">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-973">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-974">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-975">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-975">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-977">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="090f0-978">DXGI_FORMAT_R16G16B16A16 \_ snorm<sup></sup> -snorm (13)</span><span class="sxs-lookup"><span data-stu-id="090f0-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="090f0-979">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-979">Target</span></span> | <span data-ttu-id="090f0-980">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-980">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-981">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-982">64</span><span class="sxs-lookup"><span data-stu-id="090f0-982">64</span></span> |
| <span data-ttu-id="090f0-983">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-983">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-985">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-985">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-987">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-987">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-989">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-990">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-991">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-993">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-995">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-997">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-999">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-999">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1001">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1001">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1003">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1004">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1005">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1006">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1007">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1007">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1009">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1009">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1011">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1013">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1013">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1015">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1015">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1016">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1016">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1017">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1017">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1018">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1018">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1019">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1019">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1020">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1020">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1021">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1021">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1022">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1022">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1023">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1023">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1024">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1024">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1025">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1025">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1026">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1026">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1027">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1027">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1028">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1028">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1030">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1030">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1032">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1032">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1034">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1034">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1036">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1036">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1038">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1038">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1040">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1040">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1041">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1041">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1043">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1043">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1044">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1044">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1045">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1045">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1046">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1046">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1048">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1048">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="090f0-1049">DXGI_FORMAT_R16G16B16A16 \_ Sint<sup></sup> (14)</span><span class="sxs-lookup"><span data-stu-id="090f0-1049">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="090f0-1050">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1050">Target</span></span> | <span data-ttu-id="090f0-1051">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1051">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1052">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1052">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1053">64</span><span class="sxs-lookup"><span data-stu-id="090f0-1053">64</span></span> |
| <span data-ttu-id="090f0-1054">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1054">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1056">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1056">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1058">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1058">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1060">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1060">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1061">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1061">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1062">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1062">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1064">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1064">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1066">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1066">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1068">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1068">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1070">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1070">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1072">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1072">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-1073">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1073">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1074">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1074">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1075">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1075">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1076">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1076">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1077">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1077">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1079">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1079">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-1080">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1080">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1082">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1082">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1083">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1083">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1084">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1084">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1085">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1085">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1086">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1086">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1087">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1087">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1088">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1088">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1089">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1089">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1090">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1090">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1091">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1091">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1092">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1092">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1093">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1093">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1094">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1094">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1095">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1095">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1096">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1096">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1098">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1098">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1100">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1100">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1102">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1102">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1104">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1104">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-1105">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1105">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1107">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1108">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1108">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1110">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1111">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1112">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1113">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1113">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1115">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="090f0-1116">DXGI_FORMAT_R32G32 \_ Typen losen<sup>PCs</sup> (15)</span><span class="sxs-lookup"><span data-stu-id="090f0-1116">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="090f0-1117">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1117">Target</span></span> | <span data-ttu-id="090f0-1118">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1118">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1119">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1120">64</span><span class="sxs-lookup"><span data-stu-id="090f0-1120">64</span></span> |
| <span data-ttu-id="090f0-1121">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1121">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1123">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1123">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1124">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1125">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1126">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1127">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1129">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1131">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1131">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1133">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1133">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1135">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1135">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-1136">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-1137">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1138">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1139">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1139">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1140">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1141">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1141">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1143">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1143">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-1144">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1144">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1145">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1145">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1146">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1146">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1147">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1147">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1148">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1148">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1149">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1149">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1150">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1150">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1151">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1151">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1152">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1152">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1153">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1153">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1154">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1154">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1155">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1155">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1156">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1156">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1157">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1157">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1158">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1158">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1159">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1159">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1161">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1161">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1162">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1162">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1163">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1163">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-1164">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1164">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-1165">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1165">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-1166">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1166">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1167">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1167">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1169">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1170">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1171">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1172">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1172">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-1173">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="090f0-1174">DXGI_FORMAT_R32G32 \_ float<sup></sup> -Zeichen (16)</span><span class="sxs-lookup"><span data-stu-id="090f0-1174">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="090f0-1175">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1175">Target</span></span> | <span data-ttu-id="090f0-1176">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1176">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1177">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1178">64</span><span class="sxs-lookup"><span data-stu-id="090f0-1178">64</span></span> |
| <span data-ttu-id="090f0-1179">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1179">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1181">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1181">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1183">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1183">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1185">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1186">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1186">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1188">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1188">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1190">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1190">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1192">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1192">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1194">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1194">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1196">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1196">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1198">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1198">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1200">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1201">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1202">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1202">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1203">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1204">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1204">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1206">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1206">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1208">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1208">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1210">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1210">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1212">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1212">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1213">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1213">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1214">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1214">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1215">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1215">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1216">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1216">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1217">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1217">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1218">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1218">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1219">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1219">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1220">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1220">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1221">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1221">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1222">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1222">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1223">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1223">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1224">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1224">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1225">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1225">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1227">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1227">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1229">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1229">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1231">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1231">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1233">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1233">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1235">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1235">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1237">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1237">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1238">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1238">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1240">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1240">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1241">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1241">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1242">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1242">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1243">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1243">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-1244">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1244">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="090f0-1245">DXGI_FORMAT_R32G32 \_ uint<sup></sup> -Zeichen (17)</span><span class="sxs-lookup"><span data-stu-id="090f0-1245">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="090f0-1246">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1246">Target</span></span> | <span data-ttu-id="090f0-1247">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1247">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1248">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1248">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1249">64</span><span class="sxs-lookup"><span data-stu-id="090f0-1249">64</span></span> |
| <span data-ttu-id="090f0-1250">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1250">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1252">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1252">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1254">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1254">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1256">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1256">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1257">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1257">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1259">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1259">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1261">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1261">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1263">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1263">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1265">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1265">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1267">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1267">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1269">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1269">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-1270">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1270">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1271">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1271">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1272">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1272">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1273">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1273">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1274">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1274">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1276">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1276">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-1277">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1277">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1279">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1279">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1280">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1280">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1282">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1283">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1284">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1285">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1285">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1286">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1287">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1288">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1289">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1291">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1292">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1293">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1294">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1294">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1296">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1296">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1298">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1298">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1300">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1300">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1302">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1302">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-1303">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1303">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1305">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1305">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1306">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1306">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1308">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1308">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1309">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1309">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1310">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1310">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1311">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1311">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-1312">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1312">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="090f0-1313">DXGI_FORMAT_R32G32 \_ Sint<sup></sup> -Datei (18)</span><span class="sxs-lookup"><span data-stu-id="090f0-1313">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="090f0-1314">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1314">Target</span></span> | <span data-ttu-id="090f0-1315">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1315">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1316">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1316">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1317">64</span><span class="sxs-lookup"><span data-stu-id="090f0-1317">64</span></span> |
| <span data-ttu-id="090f0-1318">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1318">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1320">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1320">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1322">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1322">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1324">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1324">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1325">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1325">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1327">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1329">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1329">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1331">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1331">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1333">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1333">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1335">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1335">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1337">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1337">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-1338">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1338">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1339">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1339">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1340">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1340">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1341">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1341">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1342">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1342">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1344">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-1345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1345">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1347">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1347">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1348">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1348">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1349">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1349">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1350">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1350">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1351">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1351">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1352">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1352">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1353">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1353">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1354">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1354">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1355">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1355">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1356">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1356">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1357">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1357">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1358">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1358">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1359">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1359">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1360">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1360">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1361">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1361">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1363">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1363">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1365">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1365">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1367">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1367">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1369">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-1370">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1370">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1372">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1373">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1373">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1375">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1375">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1376">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1376">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1377">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1377">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1378">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1378">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-1379">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1379">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="090f0-1380">DXGI_FORMAT_R32G8X24 \_ Typen losen<sup>PCs</sup> (19)</span><span class="sxs-lookup"><span data-stu-id="090f0-1380">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="090f0-1381">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1381">Target</span></span> | <span data-ttu-id="090f0-1382">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1382">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1383">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1383">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1384">64</span><span class="sxs-lookup"><span data-stu-id="090f0-1384">64</span></span> |
| <span data-ttu-id="090f0-1385">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1385">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1387">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1387">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1388">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1389">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1390">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1391">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1393">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1393">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1395">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1395">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-1396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1396">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1398">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1398">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-1399">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1399">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-1400">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1400">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1401">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1401">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1402">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1402">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1403">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1403">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1404">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1404">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1406">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-1407">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1407">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1408">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1409">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1410">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1411">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1412">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1413">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1413">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1414">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1415">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1416">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1417">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1419">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1420">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1421">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1422">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1422">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1424">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1424">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1425">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1425">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1426">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1426">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-1427">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1427">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-1428">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1428">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-1429">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1429">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1430">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1430">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1432">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1433">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1434">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1435">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1435">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-1436">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="090f0-1437">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint-<sup>f</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="090f0-1437">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="090f0-1438">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1438">Target</span></span> | <span data-ttu-id="090f0-1439">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1439">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1440">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1441">64</span><span class="sxs-lookup"><span data-stu-id="090f0-1441">64</span></span> |
| <span data-ttu-id="090f0-1442">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1442">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1444">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1444">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1445">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1445">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1446">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1446">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1447">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1447">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1448">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1448">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1450">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1450">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1453">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1455">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1455">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-1456">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1456">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-1457">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1457">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1458">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1458">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1459">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1459">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1460">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1460">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1461">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1461">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1463">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-1464">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1465">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1466">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1467">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1467">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1469">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1470">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1471">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1471">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1472">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1473">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1474">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1475">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1476">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1476">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1477">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1478">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1479">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1480">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1480">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1482">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1482">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1484">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1484">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1486">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1486">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1488">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1488">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-1489">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1489">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-1490">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1490">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1491">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1491">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1493">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1494">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1495">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1496">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1496">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-1497">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="090f0-1498">DXGI_FORMAT_R32 \_ float \_ X8X24 \_ typlose<sup></sup> Rechtschreibfehler (21)</span><span class="sxs-lookup"><span data-stu-id="090f0-1498">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="090f0-1499">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1499">Target</span></span> | <span data-ttu-id="090f0-1500">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1500">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1501">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1502">64</span><span class="sxs-lookup"><span data-stu-id="090f0-1502">64</span></span> |
| <span data-ttu-id="090f0-1503">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1503">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1505">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1505">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1506">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1507">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1508">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1509">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1511">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1513">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1513">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-1514">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1514">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1516">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1516">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1518">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1518">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1520">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1520">Shader sample\_c (comparison filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1522">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1522">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1523">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1523">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1525">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1525">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1526">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1526">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1528">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1528">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-1529">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1529">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1530">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1530">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1531">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1531">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1532">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1532">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1533">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1533">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1534">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1534">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1535">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1535">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1536">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1536">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1537">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1537">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1538">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1538">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1539">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1539">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1540">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1540">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1541">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1541">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1542">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1542">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1543">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1543">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1544">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1544">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1546">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1546">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1547">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1547">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1548">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1548">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-1549">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1549">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-1550">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1550">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1552">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1552">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1553">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1553">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1555">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1555">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1556">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1556">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1557">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1557">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1558">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1558">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-1559">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1559">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="090f0-1560">DXGI_FORMAT_X32 \_ typlose \_ G8X24 \_ uint-<sup>f</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="090f0-1560">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="090f0-1561">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1561">Target</span></span> | <span data-ttu-id="090f0-1562">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1562">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1563">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1563">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1564">64</span><span class="sxs-lookup"><span data-stu-id="090f0-1564">64</span></span> |
| <span data-ttu-id="090f0-1565">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1565">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1567">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1567">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1568">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1568">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1569">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1569">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1570">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1570">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1571">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1571">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1573">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1573">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1575">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1575">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-1576">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1576">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1578">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1578">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1580">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1580">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-1581">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1581">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1582">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1582">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1583">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1583">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1584">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1584">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1585">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1585">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1587">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1587">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-1588">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1588">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1589">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1590">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1590">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1591">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1591">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1592">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1592">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1593">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1593">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1594">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1594">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1595">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1595">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1596">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1596">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1597">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1597">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1598">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1598">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1599">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1599">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1600">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1600">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1601">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1601">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1602">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1602">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1603">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1603">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1605">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1605">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1606">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1606">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1607">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1607">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-1608">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1608">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-1609">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1609">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1611">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1611">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1612">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1612">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1614">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1614">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1615">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1615">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1616">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1616">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1617">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1617">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-1618">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1618">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="090f0-1619">DXGI_FORMAT_R10G10B10A2 \_ typlosen<sup>PCs</sup> (23)</span><span class="sxs-lookup"><span data-stu-id="090f0-1619">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="090f0-1620">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1620">Target</span></span> | <span data-ttu-id="090f0-1621">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1621">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1622">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1622">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1623">32</span><span class="sxs-lookup"><span data-stu-id="090f0-1623">32</span></span> |
| <span data-ttu-id="090f0-1624">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1624">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1626">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1626">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1627">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1627">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1628">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1628">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1629">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1629">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1630">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1630">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1632">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1632">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1634">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1634">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1636">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1636">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1638">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1638">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-1639">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1639">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-1640">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1640">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1641">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1641">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1642">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1642">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1643">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1643">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1644">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1644">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1646">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1646">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-1647">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1647">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1648">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1648">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1649">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1649">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1650">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1650">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1651">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1651">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1652">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1652">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1653">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1653">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1654">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1654">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1655">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1655">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1656">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1656">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1657">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1657">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1658">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1658">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1659">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1659">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1660">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1660">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1661">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1661">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1662">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1662">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1664">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1664">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1665">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1665">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1666">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1666">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-1667">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1667">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-1668">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1668">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-1669">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1669">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1670">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1670">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1672">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1672">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1673">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1673">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1674">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1674">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1675">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1675">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1677">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1677">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="090f0-1678">DXGI_FORMAT_R10G10B10A2 \_ unorm-Datei-<sup>e</sup> /a (24)</span><span class="sxs-lookup"><span data-stu-id="090f0-1678">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="090f0-1679">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1679">Target</span></span> | <span data-ttu-id="090f0-1680">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1680">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1681">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1681">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1682">32</span><span class="sxs-lookup"><span data-stu-id="090f0-1682">32</span></span> |
| <span data-ttu-id="090f0-1683">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1683">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1685">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1685">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1687">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1687">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1689">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1689">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1690">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1690">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1691">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1691">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1693">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1693">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1695">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1697">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1697">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1699">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1699">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1701">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1701">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1703">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1703">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1704">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1704">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1705">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1705">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1706">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1706">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1707">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1707">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1709">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1709">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1711">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1711">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1713">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1713">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1715">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1715">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1716">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1716">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1717">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1717">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1718">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1718">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1719">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1719">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1720">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1720">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1721">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1721">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1722">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1722">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1723">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1723">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1724">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1724">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1725">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1725">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1726">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1726">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1727">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1727">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1728">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1728">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1730">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1730">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1732">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1732">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1734">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1734">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1736">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1736">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1738">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1738">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1740">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1740">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1742">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1742">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1744">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1744">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1745">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1745">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1747">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1747">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1749">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1749">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1751">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="090f0-1752">DXGI_FORMAT_R10G10B10A2 \_ uint<sup></sup> -Zeichen (25)</span><span class="sxs-lookup"><span data-stu-id="090f0-1752">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="090f0-1753">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1753">Target</span></span> | <span data-ttu-id="090f0-1754">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1754">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1755">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1756">32</span><span class="sxs-lookup"><span data-stu-id="090f0-1756">32</span></span> |
| <span data-ttu-id="090f0-1757">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1757">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1759">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1759">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1761">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1761">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1763">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1763">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1764">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1764">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1765">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1765">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1767">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1769">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1771">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1771">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1773">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1773">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1775">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-1776">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1777">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1778">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1778">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1779">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1780">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1780">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1782">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-1783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1783">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1785">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1786">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1786">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1788">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1788">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1789">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1789">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1790">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1790">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1791">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1791">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1792">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1792">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1793">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1793">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1794">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1794">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1795">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1795">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1796">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1796">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1797">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1797">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1798">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1798">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1799">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1799">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1800">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1800">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1802">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1802">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1804">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1804">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1806">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1806">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1808">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1808">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-1809">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1809">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1811">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1812">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1812">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1814">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1815">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1816">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1817">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1817">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1819">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="090f0-1820">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ unorm-Datei-<sup>e</sup> /a (89)</span><span class="sxs-lookup"><span data-stu-id="090f0-1820">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="090f0-1821">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1821">Target</span></span> | <span data-ttu-id="090f0-1822">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1822">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1823">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1824">32</span><span class="sxs-lookup"><span data-stu-id="090f0-1824">32</span></span> |
| <span data-ttu-id="090f0-1825">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1825">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1827">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1827">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1828">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1829">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1830">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1831">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-1832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1832">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1834">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-1835">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1835">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-1836">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1836">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-1837">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-1838">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1839">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1840">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1840">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1841">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1842">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1842">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-1843">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1843">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-1844">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1844">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1845">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1845">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1846">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1846">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1847">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1847">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1848">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1848">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1849">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1849">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1850">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1850">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1851">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1851">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1852">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1852">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1853">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1853">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1854">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1854">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1855">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1855">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1856">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1856">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1857">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1857">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1858">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1858">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1859">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1859">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1861">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1861">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1862">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1862">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1863">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1863">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-1864">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1864">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-1865">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1865">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-1866">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1866">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1868">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1868">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1870">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1870">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1871">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1871">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1873">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1873">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1875">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1875">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1877">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1877">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="090f0-1878">DXGI_FORMAT_R11G11B10 \_ float<sup></sup> -Datentyp (26)</span><span class="sxs-lookup"><span data-stu-id="090f0-1878">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="090f0-1879">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1879">Target</span></span> | <span data-ttu-id="090f0-1880">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1880">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1881">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1881">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1882">32</span><span class="sxs-lookup"><span data-stu-id="090f0-1882">32</span></span> |
| <span data-ttu-id="090f0-1883">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1883">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1885">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1885">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1887">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1887">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1889">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1890">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1891">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1893">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1893">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1895">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1895">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1897">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1897">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1899">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1899">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1901">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1901">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1903">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1904">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1905">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1905">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1906">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1907">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1907">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1909">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1909">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1911">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1911">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1913">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1913">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1915">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1915">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1916">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1916">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1917">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1917">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1918">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1918">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1919">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1919">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1920">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1920">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1921">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1921">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1922">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1922">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1923">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1923">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1924">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1924">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1925">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1925">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1926">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1926">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1927">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1927">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1928">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1928">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1930">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1930">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1932">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1932">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1934">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1934">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-1936">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1936">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1938">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1938">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1940">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1940">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1941">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1941">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-1942">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-1942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-1943">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-1944">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-1944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-1945">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1945">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-1946">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-1946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="090f0-1947">DXGI_FORMAT_R8G8B8A8 \_ typlosen<sup>PCs</sup> (27)</span><span class="sxs-lookup"><span data-stu-id="090f0-1947">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="090f0-1948">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1948">Target</span></span> | <span data-ttu-id="090f0-1949">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-1949">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-1950">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-1950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-1951">32</span><span class="sxs-lookup"><span data-stu-id="090f0-1951">32</span></span> |
| <span data-ttu-id="090f0-1952">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-1952">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1954">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1954">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1955">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-1955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1956">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-1956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1957">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-1957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-1958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-1958">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-1960">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-1962">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-1964">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1966">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-1966">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-1967">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-1968">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-1969">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-1969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-1970">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-1970">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-1971">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-1971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-1972">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1972">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1974">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-1974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-1975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1975">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1976">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1977">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-1977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-1978">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-1978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-1979">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1980">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-1980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-1981">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-1981">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-1982">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-1982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-1983">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-1984">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-1984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-1985">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-1985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-1986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-1986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-1987">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-1987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-1988">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-1988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1989">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-1989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-1990">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-1990">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-1992">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1993">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-1993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-1994">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-1994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-1995">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-1995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-1996">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-1996">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-1997">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-1997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-1998">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-1998">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2000">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2001">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2002">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2003">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2003">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2005">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="090f0-2006">DXGI_FORMAT_R8G8B8A8 \_ unorm-Datei-<sup>e</sup> /a (28)</span><span class="sxs-lookup"><span data-stu-id="090f0-2006">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="090f0-2007">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2007">Target</span></span> | <span data-ttu-id="090f0-2008">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2008">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2009">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2010">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2010">32</span></span> |
| <span data-ttu-id="090f0-2011">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2011">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2013">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2013">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2015">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2015">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2017">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2018">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2019">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2021">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2023">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2025">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2027">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2027">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2029">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2029">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2031">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2032">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2033">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2033">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2034">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2035">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2035">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2037">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2037">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2039">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2041">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2041">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2043">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-2044">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2045">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2046">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2047">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2047">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2048">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2049">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2050">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2051">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2053">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2054">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2055">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2056">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2056">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2058">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2058">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2060">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2060">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2062">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2062">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2064">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2064">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2066">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2066">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2068">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2068">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2070">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2070">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2072">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2072">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2073">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2073">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2075">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2075">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2077">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2077">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2079">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2079">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="090f0-2080">DXGI_FORMAT_R8G8B8A8 \_ unorm \_ sRGB-<sup>FICS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="090f0-2080">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="090f0-2081">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2081">Target</span></span> | <span data-ttu-id="090f0-2082">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2082">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2083">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2083">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2084">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2084">32</span></span> |
| <span data-ttu-id="090f0-2085">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2085">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2087">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2087">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2088">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2088">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2089">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2089">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2090">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2090">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2091">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2091">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2093">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2093">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2095">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2095">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2097">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2097">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2099">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2099">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2101">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2101">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2103">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2103">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2104">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2104">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2105">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2105">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2106">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2106">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2107">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2107">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2109">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2109">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2111">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2113">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2113">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2115">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-2116">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2117">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2118">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2119">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2119">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2120">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2121">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2122">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2123">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2124">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2124">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2125">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2126">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2127">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2128">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2128">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2130">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2130">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2132">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2132">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2134">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2134">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2136">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2136">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2138">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2138">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2140">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2140">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2142">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2142">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2144">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2145">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2145">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2147">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2147">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2149">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2149">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2151">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2151">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="090f0-2152">DXGI_FORMAT_R8G8B8A8 \_ uint<sup></sup> -Zeichen (30)</span><span class="sxs-lookup"><span data-stu-id="090f0-2152">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="090f0-2153">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2153">Target</span></span> | <span data-ttu-id="090f0-2154">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2154">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2155">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2155">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2156">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2156">32</span></span> |
| <span data-ttu-id="090f0-2157">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2157">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2159">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2159">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2161">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2161">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2163">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2163">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2164">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2164">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2165">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2165">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2167">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2167">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2169">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2169">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2171">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2171">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2173">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2173">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2175">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2175">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-2176">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2176">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2177">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2177">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2178">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2178">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2179">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2179">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2180">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2180">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2182">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2182">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-2183">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2183">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2185">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2185">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2186">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2186">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2188">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2188">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2189">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2189">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2190">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2190">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2191">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2191">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2192">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2192">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2193">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2193">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2194">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2194">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2195">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2195">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2196">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2196">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2197">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2197">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2198">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2198">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2199">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2199">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2200">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2200">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2202">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2202">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2204">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2204">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2206">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2206">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2208">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2208">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-2209">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2209">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2211">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2211">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-2212">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2212">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2214">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2214">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2215">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2215">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2216">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2216">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2217">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2217">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2219">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2219">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="090f0-2220">DXGI_FORMAT_R8G8B8A8 \_ snorm<sup></sup> -snorm (31)</span><span class="sxs-lookup"><span data-stu-id="090f0-2220">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="090f0-2221">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2221">Target</span></span> | <span data-ttu-id="090f0-2222">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2222">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2223">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2223">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2224">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2224">32</span></span> |
| <span data-ttu-id="090f0-2225">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2225">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2227">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2227">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2229">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2229">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2231">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2232">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2233">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2235">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2235">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2237">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2237">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2239">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2241">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2241">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2243">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2243">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2245">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2246">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2247">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2248">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2249">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2249">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2251">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2251">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2253">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2253">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2255">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2255">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2257">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2257">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-2258">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2258">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2259">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2259">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2260">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2260">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2261">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2261">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2262">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2262">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2263">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2263">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2264">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2264">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2265">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2265">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2266">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2266">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2267">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2267">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2268">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2268">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2269">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2269">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2270">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2270">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2272">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2272">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2274">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2274">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2276">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2276">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2278">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2278">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2280">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2280">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2282">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-2283">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2283">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2285">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2285">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2286">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2286">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2287">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2287">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2288">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2288">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2290">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="090f0-2291">DXGI_FORMAT_R8G8B8A8 \_ Sint<sup></sup> -Werte (32)</span><span class="sxs-lookup"><span data-stu-id="090f0-2291">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="090f0-2292">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2292">Target</span></span> | <span data-ttu-id="090f0-2293">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2293">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2294">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2295">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2295">32</span></span> |
| <span data-ttu-id="090f0-2296">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2296">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2298">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2298">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2300">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2300">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2302">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2303">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2304">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2306">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2306">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2308">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2308">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2310">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2310">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2312">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2312">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2314">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2314">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-2315">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2316">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2317">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2317">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2318">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2319">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2319">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2321">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-2322">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2322">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2324">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2324">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2325">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2325">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-2326">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2326">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2327">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2327">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2328">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2328">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2329">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2329">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2330">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2330">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2331">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2331">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2332">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2332">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2333">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2333">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2334">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2334">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2335">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2335">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2336">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2336">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2337">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2337">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2338">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2338">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2340">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2340">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2342">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2342">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2344">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2344">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2346">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2346">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-2347">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2347">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2349">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2349">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-2350">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2350">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2352">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2352">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2353">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2353">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2354">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2354">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2355">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2355">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2357">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2357">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="090f0-2358">DXGI_FORMAT_R16G16 \_ Typen losen<sup>PCs</sup> (33)</span><span class="sxs-lookup"><span data-stu-id="090f0-2358">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="090f0-2359">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2359">Target</span></span> | <span data-ttu-id="090f0-2360">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2360">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2361">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2361">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2362">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2362">32</span></span> |
| <span data-ttu-id="090f0-2363">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2363">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2365">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2365">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2366">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2366">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2367">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2367">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2368">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2368">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2369">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2369">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2371">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2371">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2373">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2373">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2375">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2375">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2377">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2377">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-2378">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2378">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-2379">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2379">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2380">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2380">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2381">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2381">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2382">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2382">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2383">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2383">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2385">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2385">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-2386">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2386">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2387">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2387">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2388">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2388">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-2389">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2389">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2390">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2390">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2391">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2391">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2392">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2392">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2393">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2393">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2394">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2394">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2395">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2395">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2396">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2396">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2397">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2397">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2398">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2398">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2399">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2399">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2400">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2400">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2401">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2401">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2403">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2403">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2404">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2404">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2405">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2405">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-2406">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2406">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-2407">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2407">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-2408">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2408">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-2409">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2409">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2411">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2411">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2412">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2412">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2413">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2413">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2414">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2414">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-2415">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2415">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="090f0-2416">DXGI_FORMAT_R16G16 \_ float<sup></sup> -Zeichen (34)</span><span class="sxs-lookup"><span data-stu-id="090f0-2416">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="090f0-2417">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2417">Target</span></span> | <span data-ttu-id="090f0-2418">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2418">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2419">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2419">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2420">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2420">32</span></span> |
| <span data-ttu-id="090f0-2421">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2421">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2423">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2423">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2425">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2425">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2427">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2427">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2428">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2428">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2429">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2429">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2431">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2431">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2433">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2433">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2435">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2435">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2437">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2437">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2439">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2439">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2441">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2442">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2443">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2443">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2444">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2445">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2445">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2447">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2447">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2449">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2449">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2451">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2451">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2453">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-2454">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2455">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2456">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2457">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2457">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2458">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2459">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2460">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2461">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2462">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2462">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2463">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2464">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2465">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2466">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2466">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2468">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2468">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2470">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2470">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2472">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2472">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2474">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2474">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2476">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2476">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2478">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-2479">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2479">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2481">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2482">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2483">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2484">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2484">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-2485">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="090f0-2486">DXGI_FORMAT_R16G16 \_ unorm-Datei-<sup>e</sup> /a (35)</span><span class="sxs-lookup"><span data-stu-id="090f0-2486">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="090f0-2487">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2487">Target</span></span> | <span data-ttu-id="090f0-2488">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2488">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2489">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2490">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2490">32</span></span> |
| <span data-ttu-id="090f0-2491">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2491">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2493">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2493">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2495">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2495">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2497">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2497">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2498">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2498">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2499">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2499">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2501">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2503">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2503">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2505">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2507">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2507">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2509">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2509">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2511">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2512">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2513">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2514">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2515">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2515">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2517">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2517">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2519">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2519">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2521">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2521">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2523">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2523">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-2524">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2524">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2525">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2525">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2526">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2526">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2527">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2527">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2528">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2528">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2529">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2529">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2530">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2530">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2531">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2531">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2532">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2532">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2533">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2533">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2534">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2534">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2535">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2535">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2536">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2536">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2538">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2538">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2540">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2540">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2542">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2542">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2544">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2544">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2546">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2546">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2548">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2548">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-2549">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2549">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2551">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2551">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2552">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2552">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2553">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2553">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2554">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2554">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-2555">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2555">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="090f0-2556">DXGI_FORMAT_R16G16 \_ uint-<sup>f</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="090f0-2556">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="090f0-2557">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2557">Target</span></span> | <span data-ttu-id="090f0-2558">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2558">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2559">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2559">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2560">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2560">32</span></span> |
| <span data-ttu-id="090f0-2561">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2561">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2563">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2563">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2565">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2565">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2567">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2567">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2568">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2568">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2569">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2569">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2571">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2571">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2573">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2573">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2575">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2575">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2577">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2577">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2579">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2579">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-2580">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2580">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2581">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2581">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2582">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2582">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2583">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2583">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2584">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2584">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2586">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2586">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-2587">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2587">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2589">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2590">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2590">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2592">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2592">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2593">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2593">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2594">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2594">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2595">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2595">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2596">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2596">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2597">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2597">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2598">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2598">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2599">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2599">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2600">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2600">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2601">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2601">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2602">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2602">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2603">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2603">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2604">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2604">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2606">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2606">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2608">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2608">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2610">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2610">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2612">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2612">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-2613">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2613">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2615">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2615">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-2616">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2616">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2618">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2618">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2619">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2619">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2620">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2620">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2621">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2621">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-2622">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2622">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="090f0-2623">DXGI_FORMAT_R16G16 \_ snorm<sup></sup> -snorm (37)</span><span class="sxs-lookup"><span data-stu-id="090f0-2623">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="090f0-2624">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2624">Target</span></span> | <span data-ttu-id="090f0-2625">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2625">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2626">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2626">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2627">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2627">32</span></span> |
| <span data-ttu-id="090f0-2628">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2628">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2630">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2630">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2632">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2632">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2634">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2634">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2635">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2635">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2636">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2636">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2638">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2638">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2640">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2640">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2642">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2642">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2644">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2644">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2646">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2646">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2648">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2649">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2650">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2650">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2651">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2652">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2652">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2654">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2654">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2656">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2656">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2658">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2658">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2660">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2660">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-2661">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2661">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2662">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2662">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2663">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2663">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2664">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2664">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2665">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2665">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2666">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2666">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2667">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2667">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2668">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2668">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2669">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2669">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2670">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2670">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2671">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2671">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2672">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2672">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2673">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2673">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2675">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2675">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2677">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2677">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2679">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2679">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2681">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2681">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2683">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2683">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2685">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2685">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-2686">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2686">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2688">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2688">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2689">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2689">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2690">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2690">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2691">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2691">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-2692">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2692">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="090f0-2693">DXGI_FORMAT_R16G16 \_ Sint<sup></sup> -Werte (38)</span><span class="sxs-lookup"><span data-stu-id="090f0-2693">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="090f0-2694">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2694">Target</span></span> | <span data-ttu-id="090f0-2695">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2695">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2696">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2696">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2697">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2697">32</span></span> |
| <span data-ttu-id="090f0-2698">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2698">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2700">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2700">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2702">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2702">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2704">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2705">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2706">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2708">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2708">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2710">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2710">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2712">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2712">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2714">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2714">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2716">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-2717">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2718">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2719">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2720">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2721">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2721">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2723">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-2724">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2724">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2726">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2726">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2727">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2727">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-2728">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2728">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2729">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2729">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2730">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2730">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2731">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2731">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2732">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2732">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2733">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2733">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2734">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2734">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2735">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2735">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2736">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2736">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2737">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2737">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2738">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2738">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2739">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2739">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2740">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2740">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2742">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2742">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2744">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2744">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2746">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2746">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2748">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2748">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-2749">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2749">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2751">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-2752">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2752">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2754">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2755">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2756">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2757">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2757">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-2758">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="090f0-2759">DXGI_FORMAT_R32 \_ Typen losen<sup>PCs</sup> (39)</span><span class="sxs-lookup"><span data-stu-id="090f0-2759">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="090f0-2760">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2760">Target</span></span> | <span data-ttu-id="090f0-2761">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2761">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2762">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2763">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2763">32</span></span> |
| <span data-ttu-id="090f0-2764">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2764">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2766">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2766">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2767">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2768">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2769">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2770">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2772">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2774">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2776">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2778">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2778">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-2779">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2779">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-2780">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2780">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2781">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2781">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2782">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2782">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2783">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2783">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2784">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2784">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2786">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2786">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-2787">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2787">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2788">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2788">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2789">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2789">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-2790">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2790">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2791">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2791">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2792">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2792">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2793">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2793">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2794">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2794">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2795">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2795">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2796">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2796">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2797">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2797">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2798">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2798">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2799">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2799">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2800">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2800">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2801">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2801">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2802">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2802">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2804">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2804">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2805">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2805">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2806">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2806">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-2807">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2807">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-2808">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2808">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-2809">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2809">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-2810">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2810">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2812">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2812">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2813">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2813">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2814">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2814">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2815">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2815">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2817">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2817">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="090f0-2818">DXGI_FORMAT_D32 \_ float<sup></sup> -Zeichen (40)</span><span class="sxs-lookup"><span data-stu-id="090f0-2818">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="090f0-2819">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2819">Target</span></span> | <span data-ttu-id="090f0-2820">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2820">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2821">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2821">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2822">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2822">32</span></span> |
| <span data-ttu-id="090f0-2823">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2823">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2825">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2825">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2826">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2826">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2827">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2827">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2828">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2828">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2829">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2829">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2831">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2831">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2833">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2833">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-2834">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2834">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2836">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2836">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-2837">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-2838">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2839">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2840">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2840">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2841">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2842">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2842">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2844">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2844">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-2845">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2845">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2846">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2846">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2847">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2847">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-2848">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2848">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2850">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2850">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2851">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2851">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2852">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2852">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2853">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2853">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2854">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2854">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2855">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2855">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2856">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2856">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2857">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2857">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2858">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2858">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2859">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2859">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2860">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2860">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2861">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2861">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2863">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2863">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2865">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2865">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2867">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2867">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2869">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-2870">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2870">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-2871">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-2872">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2872">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2874">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2875">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2876">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2877">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2877">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2879">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="090f0-2880">DXGI_FORMAT_R32 \_ float<sup></sup> -Zeichen (41)</span><span class="sxs-lookup"><span data-stu-id="090f0-2880">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="090f0-2881">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2881">Target</span></span> | <span data-ttu-id="090f0-2882">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2882">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2883">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2884">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2884">32</span></span> |
| <span data-ttu-id="090f0-2885">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2885">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2887">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2887">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2889">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2889">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2891">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2891">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-2892">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2892">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2894">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2894">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2896">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2896">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2898">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2898">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2900">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2902">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2902">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2904">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2904">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2906">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2906">Shader sample\_c (comparison filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2908">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2908">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2909">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2909">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2911">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2911">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2912">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2912">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2914">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2914">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2916">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2916">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2918">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2918">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2920">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2920">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-2921">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2921">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2922">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2922">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2923">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2923">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2924">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2924">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2925">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2925">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2926">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2926">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2927">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2927">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2928">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2928">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-2929">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-2929">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-2930">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-2930">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-2931">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-2931">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2932">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-2932">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-2933">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-2933">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2935">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2935">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2937">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2937">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2939">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-2939">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2941">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-2941">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2943">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2943">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2945">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-2945">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-2946">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-2946">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2948">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-2948">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-2949">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2949">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-2950">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-2950">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-2951">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2951">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2953">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-2953">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="090f0-2954">DXGI_FORMAT_R32 \_ uint-<sup>f</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="090f0-2954">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="090f0-2955">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2955">Target</span></span> | <span data-ttu-id="090f0-2956">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-2956">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-2957">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-2957">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-2958">32</span><span class="sxs-lookup"><span data-stu-id="090f0-2958">32</span></span> |
| <span data-ttu-id="090f0-2959">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-2959">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2961">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2961">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2963">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-2963">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2965">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-2965">Input Assembler Index Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2967">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-2967">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-2969">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2971">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-2971">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2973">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-2973">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-2975">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2977">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-2977">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2979">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2979">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-2980">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2980">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-2981">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-2981">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-2982">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-2982">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-2983">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-2983">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-2984">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2984">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2986">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-2987">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2987">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-2989">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-2989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-2990">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-2990">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-2992">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-2992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-2993">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2994">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-2994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-2995">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-2995">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-2996">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-2996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-2997">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-2997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-2998">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-2998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-2999">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-2999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3000">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3000">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3001">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3002">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3003">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3004">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3004">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3006">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3006">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3008">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3008">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3010">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3010">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3012">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3012">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-3013">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3013">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3015">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3015">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3016">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3016">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3018">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3018">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3019">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3019">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3020">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3020">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3021">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3021">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3023">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3023">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="090f0-3024">DXGI_FORMAT_R32 \_ Sint<sup></sup> -Werte (43)</span><span class="sxs-lookup"><span data-stu-id="090f0-3024">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="090f0-3025">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3025">Target</span></span> | <span data-ttu-id="090f0-3026">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3026">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3027">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3027">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3028">32</span><span class="sxs-lookup"><span data-stu-id="090f0-3028">32</span></span> |
| <span data-ttu-id="090f0-3029">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3029">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3031">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3031">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3033">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3033">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3035">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3035">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3036">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3036">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3038">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3038">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3040">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3040">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3042">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3042">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3044">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3044">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3046">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3046">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3048">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3048">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-3049">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3049">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3050">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3050">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3051">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3051">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-3052">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3052">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3053">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3053">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3055">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3055">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-3056">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3056">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3058">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3058">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3059">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3059">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3060">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3060">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3061">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3061">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3062">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3062">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3063">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3063">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3064">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3064">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3065">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3065">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3066">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3066">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3067">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3067">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3068">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3068">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3069">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3069">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3070">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3070">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3071">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3071">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3072">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3072">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3074">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3074">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3076">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3076">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3078">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3078">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3080">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-3081">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3081">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3083">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3083">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3084">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3084">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3086">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3087">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3088">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3089">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3089">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3091">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="090f0-3092">DXGI_FORMAT_R24G8 \_ Typen losen<sup>PCs</sup> (44)</span><span class="sxs-lookup"><span data-stu-id="090f0-3092">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="090f0-3093">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3093">Target</span></span> | <span data-ttu-id="090f0-3094">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3094">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3095">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3096">32</span><span class="sxs-lookup"><span data-stu-id="090f0-3096">32</span></span> |
| <span data-ttu-id="090f0-3097">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3097">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3099">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3099">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3100">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3101">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3102">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3103">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3105">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3105">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3107">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3107">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-3108">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3108">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3110">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3110">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-3111">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3111">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-3112">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3112">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3113">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3113">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3114">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3114">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-3115">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3115">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3116">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3116">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3118">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3118">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-3119">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3119">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3120">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3120">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3121">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3121">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3122">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3122">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3123">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3123">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3124">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3124">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3125">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3125">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3126">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3126">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3127">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3127">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3128">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3128">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3129">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3129">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3130">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3130">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3131">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3131">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3132">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3132">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3133">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3133">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3134">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3134">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3136">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3136">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3137">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3137">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3138">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3138">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-3139">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3139">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-3140">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3140">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-3141">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3141">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3142">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3142">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3144">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3145">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3145">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3146">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3146">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3147">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3147">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-3148">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3148">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="090f0-3149">DXGI_FORMAT_D24 \_ unorm \_ S8 \_ uint<sup></sup> -Zeichen (45)</span><span class="sxs-lookup"><span data-stu-id="090f0-3149">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="090f0-3150">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3150">Target</span></span> | <span data-ttu-id="090f0-3151">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3151">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3152">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3152">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3153">32</span><span class="sxs-lookup"><span data-stu-id="090f0-3153">32</span></span> |
| <span data-ttu-id="090f0-3154">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3154">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3156">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3156">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3157">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3157">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3158">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3158">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3159">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3159">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3160">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3160">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3162">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3162">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3164">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3164">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-3165">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3165">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3167">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3167">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-3168">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3168">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-3169">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3169">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3170">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3170">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3171">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3171">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-3172">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3173">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3173">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3175">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3175">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-3176">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3176">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3177">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3177">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3178">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3178">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3179">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3179">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3181">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3181">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3182">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3182">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3183">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3183">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3184">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3184">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3185">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3185">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3186">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3186">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3187">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3187">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3188">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3188">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3189">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3189">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3190">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3190">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3191">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3191">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3192">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3192">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3194">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3194">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3196">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3196">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3198">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3198">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3200">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3200">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-3201">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3201">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-3202">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3202">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3203">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3203">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3205">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3205">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3206">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3206">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3207">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3207">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3208">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3208">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-3209">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3209">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="090f0-3210">DXGI_FORMAT_R24 \_ unorm \_ X8- \_ typlosen<sup>f</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="090f0-3210">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="090f0-3211">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3211">Target</span></span> | <span data-ttu-id="090f0-3212">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3212">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3213">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3213">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3214">32</span><span class="sxs-lookup"><span data-stu-id="090f0-3214">32</span></span> |
| <span data-ttu-id="090f0-3215">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3215">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3217">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3217">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3218">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3218">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3219">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3219">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3220">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3220">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3221">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3221">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3223">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3223">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3225">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3225">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-3226">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3226">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3228">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3228">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3230">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3230">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3232">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3232">Shader sample\_c (comparison filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3234">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3234">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3235">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3235">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3237">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3237">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3238">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3238">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3240">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3240">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-3241">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3241">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3242">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3242">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3243">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3243">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3244">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3244">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3245">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3245">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3246">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3246">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3247">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3247">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3248">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3248">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3249">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3249">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3250">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3250">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3251">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3251">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3252">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3252">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3253">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3253">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3254">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3254">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3255">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3255">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3256">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3256">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3258">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3258">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3259">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3259">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3260">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3260">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-3261">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3261">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-3262">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3262">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3264">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3264">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3265">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3265">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3267">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3267">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3268">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3268">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3269">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3269">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3270">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3270">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-3271">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="090f0-3272">DXGI_FORMAT_X24 \_ typlose \_ G8 \_ uint<sup></sup> -Zeichen (47)</span><span class="sxs-lookup"><span data-stu-id="090f0-3272">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="090f0-3273">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3273">Target</span></span> | <span data-ttu-id="090f0-3274">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3274">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3275">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3276">32</span><span class="sxs-lookup"><span data-stu-id="090f0-3276">32</span></span> |
| <span data-ttu-id="090f0-3277">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3277">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3279">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3279">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3280">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3281">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3282">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3283">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3285">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3285">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3287">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3287">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-3288">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3288">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3290">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3290">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3292">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3292">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-3293">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3293">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3294">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3294">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3295">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3295">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-3296">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3297">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3297">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3299">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-3300">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3300">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3301">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3302">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3303">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3304">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3305">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3306">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3306">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3307">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3308">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3309">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3310">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3311">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3312">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3313">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3314">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3315">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3315">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3317">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3318">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3319">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-3320">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-3321">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3321">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3323">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3323">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3324">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3324">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3326">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3327">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3328">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3329">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-3330">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="090f0-3331">DXGI_FORMAT_R8G8 \_ Typen losen<sup>PCs</sup> (48)</span><span class="sxs-lookup"><span data-stu-id="090f0-3331">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="090f0-3332">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3332">Target</span></span> | <span data-ttu-id="090f0-3333">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3334">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3335">16</span><span class="sxs-lookup"><span data-stu-id="090f0-3335">16</span></span> |
| <span data-ttu-id="090f0-3336">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3336">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3338">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3338">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3339">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3339">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3340">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3340">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3341">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3341">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3342">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3342">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3344">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3344">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3346">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3346">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3348">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3350">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3350">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-3351">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3351">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-3352">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3352">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3353">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3353">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3354">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3354">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-3355">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3355">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3356">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3356">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3358">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3358">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-3359">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3359">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3360">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3360">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3361">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3361">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3362">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3362">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3363">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3363">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3364">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3364">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3365">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3365">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3366">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3366">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3367">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3367">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3368">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3368">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3369">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3369">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3370">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3370">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3371">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3371">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3372">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3372">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3373">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3373">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3374">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3374">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3376">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3376">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3377">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3377">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3378">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3378">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-3379">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3379">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-3380">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3380">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-3381">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3382">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3382">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3384">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3385">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3386">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3387">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3387">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-3388">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3388">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="090f0-3389">DXGI_FORMAT_R8G8 \_ unorm-Datei-<sup>e</sup> /a (49)</span><span class="sxs-lookup"><span data-stu-id="090f0-3389">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="090f0-3390">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3390">Target</span></span> | <span data-ttu-id="090f0-3391">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3391">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3392">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3392">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3393">16</span><span class="sxs-lookup"><span data-stu-id="090f0-3393">16</span></span> |
| <span data-ttu-id="090f0-3394">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3394">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3396">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3396">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3398">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3398">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3400">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3400">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3401">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3401">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3402">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3402">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3404">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3406">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3406">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3408">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3408">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3410">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3410">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3412">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3412">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3414">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3415">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3416">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3416">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-3417">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3418">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3418">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3420">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3420">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3422">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3424">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3424">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3426">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3427">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3428">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3429">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3430">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3430">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3431">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3432">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3433">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3434">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3435">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3436">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3437">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3438">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3439">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3439">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3441">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3441">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3443">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3443">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3445">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3445">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3447">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3447">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3449">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3449">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3451">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3451">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3452">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3452">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3454">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3454">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3455">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3455">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3456">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3456">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3457">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3457">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3459">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3459">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="090f0-3460">DXGI_FORMAT_R8G8 \_ uint-<sup>f</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="090f0-3460">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="090f0-3461">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3461">Target</span></span> | <span data-ttu-id="090f0-3462">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3462">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3463">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3463">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3464">16</span><span class="sxs-lookup"><span data-stu-id="090f0-3464">16</span></span> |
| <span data-ttu-id="090f0-3465">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3465">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3467">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3467">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3469">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3469">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3471">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3471">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3472">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3472">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3473">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3473">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3475">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3475">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3477">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3477">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3479">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3479">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3481">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3481">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3483">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3483">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-3484">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3484">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3485">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3485">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3486">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3486">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-3487">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3487">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3488">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3488">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3490">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3490">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-3491">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3491">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3493">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3493">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3494">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3494">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3496">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3496">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3497">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3497">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3498">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3498">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3499">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3499">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3500">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3500">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3501">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3501">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3502">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3502">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3503">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3503">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3504">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3504">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3505">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3505">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3506">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3506">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3507">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3507">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3508">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3508">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3510">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3510">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3512">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3512">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3514">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3514">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3516">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3516">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-3517">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3517">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3519">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3520">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3520">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3522">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3523">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3524">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3525">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3525">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-3526">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="090f0-3527">DXGI_FORMAT_R8G8 \_ snorm<sup></sup> -snorm (51)</span><span class="sxs-lookup"><span data-stu-id="090f0-3527">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="090f0-3528">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3528">Target</span></span> | <span data-ttu-id="090f0-3529">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3529">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3530">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3531">16</span><span class="sxs-lookup"><span data-stu-id="090f0-3531">16</span></span> |
| <span data-ttu-id="090f0-3532">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3532">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3534">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3534">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3536">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3536">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3538">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3539">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3540">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3542">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3542">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3544">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3544">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3546">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3546">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3548">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3548">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3550">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3550">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3552">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3553">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3554">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3554">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-3555">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3556">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3556">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3558">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3558">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3560">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3560">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3562">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3562">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3564">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3565">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3566">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3567">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3568">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3568">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3569">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3570">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3571">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3572">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3573">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3573">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3574">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3575">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3576">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3577">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3577">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3579">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3579">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3581">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3581">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3583">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3583">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3585">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3585">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3587">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3587">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3589">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3589">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3590">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3590">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3592">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3592">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3593">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3593">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3594">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3594">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3595">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3595">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-3596">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3596">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="090f0-3597">DXGI_FORMAT_R8G8 \_ Sint<sup></sup> -Werte (52)</span><span class="sxs-lookup"><span data-stu-id="090f0-3597">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="090f0-3598">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3598">Target</span></span> | <span data-ttu-id="090f0-3599">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3599">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3600">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3600">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3601">16</span><span class="sxs-lookup"><span data-stu-id="090f0-3601">16</span></span> |
| <span data-ttu-id="090f0-3602">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3602">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3604">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3604">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3606">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3606">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3608">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3609">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3610">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3612">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3612">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3614">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3614">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3616">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3616">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3618">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3618">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3620">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3620">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-3621">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3621">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3622">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3622">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3623">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3623">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-3624">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3624">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3625">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3625">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3627">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3627">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-3628">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3628">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3630">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3630">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3631">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3631">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3632">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3632">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3633">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3633">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3634">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3634">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3635">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3635">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3636">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3636">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3637">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3637">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3638">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3638">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3639">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3639">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3640">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3640">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3641">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3641">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3642">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3642">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3643">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3643">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3644">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3644">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3646">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3646">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3648">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3648">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3650">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3650">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3652">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-3653">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3653">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3655">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3655">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3656">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3656">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3658">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3658">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3659">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3659">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3660">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3660">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3661">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3661">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-3662">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3662">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="090f0-3663">DXGI_FORMAT_R16 \_ Typen losen<sup>PCs</sup> (53)</span><span class="sxs-lookup"><span data-stu-id="090f0-3663">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="090f0-3664">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3664">Target</span></span> | <span data-ttu-id="090f0-3665">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3665">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3666">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3666">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3667">16</span><span class="sxs-lookup"><span data-stu-id="090f0-3667">16</span></span> |
| <span data-ttu-id="090f0-3668">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3668">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3670">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3670">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3671">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3672">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3673">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3674">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3676">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3676">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3678">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3678">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3680">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3680">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3682">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3682">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-3683">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3683">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-3684">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3685">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3686">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3686">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-3687">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3688">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3688">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3690">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-3691">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3691">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3692">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3693">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3694">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3695">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3696">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3697">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3697">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3698">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3699">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3700">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3701">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3702">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3703">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3704">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3705">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3706">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3706">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3708">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3709">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3710">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-3711">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-3712">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3712">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-3713">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3714">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3714">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3716">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3716">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3717">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3717">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3718">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3718">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3719">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3719">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3721">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3721">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="090f0-3722">DXGI_FORMAT_R16 \_ float<sup></sup> -Zeichen (54)</span><span class="sxs-lookup"><span data-stu-id="090f0-3722">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="090f0-3723">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3723">Target</span></span> | <span data-ttu-id="090f0-3724">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3724">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3725">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3725">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3726">16</span><span class="sxs-lookup"><span data-stu-id="090f0-3726">16</span></span> |
| <span data-ttu-id="090f0-3727">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3727">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3729">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3729">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3731">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3731">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3733">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3734">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3735">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3737">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3739">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3741">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3743">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3743">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3745">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3745">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3747">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3748">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3749">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3749">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3751">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3752">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3752">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3754">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3754">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3756">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3756">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3758">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3758">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3760">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3760">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3761">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3761">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3762">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3762">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3763">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3763">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3764">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3764">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3765">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3765">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3766">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3766">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3767">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3767">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3768">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3768">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3769">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3769">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3770">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3770">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3771">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3771">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3772">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3772">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3773">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3773">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3775">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3775">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3777">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3777">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3779">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3779">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3781">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3781">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3783">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3783">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3785">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3785">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3786">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3786">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3788">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3788">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3789">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3789">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3790">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3790">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3791">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3791">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3793">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3793">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="090f0-3794">DXGI_FORMAT_D16 \_ unorm-Datei-<sup>e</sup> /a (55)</span><span class="sxs-lookup"><span data-stu-id="090f0-3794">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="090f0-3795">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3795">Target</span></span> | <span data-ttu-id="090f0-3796">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3796">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3797">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3797">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3798">16</span><span class="sxs-lookup"><span data-stu-id="090f0-3798">16</span></span> |
| <span data-ttu-id="090f0-3799">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3799">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3801">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3801">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3802">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3802">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3803">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3803">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3804">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3804">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3805">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3805">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3807">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3810">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3812">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3812">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-3813">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3813">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-3814">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3814">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3815">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3815">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3816">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3816">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-3817">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3817">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3818">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3818">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3820">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3820">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-3821">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3821">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3822">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3822">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3823">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3823">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3824">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3824">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3826">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3826">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3827">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3827">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3828">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3828">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3829">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3829">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3830">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3830">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3831">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3831">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3832">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3832">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3833">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3833">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3834">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3834">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3835">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3835">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3836">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3836">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3837">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3837">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3839">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3839">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3841">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3841">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3843">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3843">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3845">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3845">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-3846">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3846">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-3847">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3847">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3848">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3848">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3850">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3850">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3851">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3851">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3852">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3852">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3853">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3853">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3855">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3855">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="090f0-3856">DXGI_FORMAT_R16 \_ unorm-Datei-<sup>e</sup> /a (56)</span><span class="sxs-lookup"><span data-stu-id="090f0-3856">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="090f0-3857">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3857">Target</span></span> | <span data-ttu-id="090f0-3858">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3858">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3859">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3859">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3860">16</span><span class="sxs-lookup"><span data-stu-id="090f0-3860">16</span></span> |
| <span data-ttu-id="090f0-3861">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3861">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3863">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3863">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3865">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3865">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3867">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3868">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3869">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3871">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3871">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3873">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3873">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3875">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3875">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3877">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3877">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3879">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3879">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3881">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3881">Shader sample\_c (comparison filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3883">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3883">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3884">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3884">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3886">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3886">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3887">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3887">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3889">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3889">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3891">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3891">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3893">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3893">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3895">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3895">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-3896">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3896">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3897">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3897">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3898">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3898">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3899">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3899">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3900">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3900">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3901">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3901">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3902">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3902">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3903">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3903">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3904">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3904">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3905">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3905">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3906">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3906">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3907">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3907">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3908">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3908">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3910">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3910">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3912">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3912">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3914">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3914">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3916">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3916">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3918">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3918">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3920">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3920">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3921">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3921">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3923">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3923">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3924">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3924">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3925">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3925">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3926">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3926">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3928">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="090f0-3929">DXGI_FORMAT_R16 \_ uint-<sup>f</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="090f0-3929">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="090f0-3930">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3930">Target</span></span> | <span data-ttu-id="090f0-3931">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-3931">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-3932">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-3932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-3933">16</span><span class="sxs-lookup"><span data-stu-id="090f0-3933">16</span></span> |
| <span data-ttu-id="090f0-3934">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-3934">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3936">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3936">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3938">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-3938">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3940">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-3940">Input Assembler Index Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3942">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-3942">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-3943">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-3943">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3945">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-3945">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3947">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-3947">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3949">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-3949">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3951">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-3951">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3953">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-3954">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-3955">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-3955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-3956">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-3956">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-3957">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-3957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-3958">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3958">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3960">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-3960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-3961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3961">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3963">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-3964">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-3964">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3966">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3966">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-3967">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3967">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3968">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-3968">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-3969">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-3969">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-3970">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-3970">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-3971">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3971">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-3972">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-3972">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-3973">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-3973">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-3974">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-3974">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-3975">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-3975">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-3976">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-3976">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3977">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-3977">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-3978">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-3978">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3980">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3980">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3982">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-3982">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3984">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-3984">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-3986">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-3986">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-3987">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-3987">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3989">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-3989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-3990">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-3990">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3992">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-3992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-3993">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-3994">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-3994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-3995">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3995">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-3997">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-3997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="090f0-3998">DXGI_FORMAT_R16 \_ snorm<sup></sup> -snorm (58)</span><span class="sxs-lookup"><span data-stu-id="090f0-3998">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="090f0-3999">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-3999">Target</span></span> | <span data-ttu-id="090f0-4000">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4000">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4001">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4002">16</span><span class="sxs-lookup"><span data-stu-id="090f0-4002">16</span></span> |
| <span data-ttu-id="090f0-4003">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4003">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4005">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4005">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4007">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4007">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4009">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4009">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4010">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4010">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4011">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4011">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4013">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4013">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4015">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4015">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4017">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4017">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4019">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4019">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4021">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4021">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4023">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4023">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4024">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4024">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4025">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4025">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4027">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4027">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4028">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4028">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4030">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4030">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4032">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4032">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4034">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4034">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4036">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4036">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4037">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4037">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4038">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4038">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4039">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4039">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4040">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4040">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4041">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4041">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4042">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4042">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4043">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4043">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4044">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4044">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4045">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4045">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4046">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4046">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4047">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4047">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4048">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4048">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4049">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4049">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4051">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4051">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4053">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4053">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4055">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4055">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4057">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4057">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4059">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4059">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4061">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4062">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4062">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4064">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4064">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4065">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4065">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4066">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4066">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4067">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4067">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4069">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4069">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="090f0-4070">DXGI_FORMAT_R16 \_ Sint<sup></sup> -Werte (59)</span><span class="sxs-lookup"><span data-stu-id="090f0-4070">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="090f0-4071">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4071">Target</span></span> | <span data-ttu-id="090f0-4072">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4072">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4073">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4073">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4074">16</span><span class="sxs-lookup"><span data-stu-id="090f0-4074">16</span></span> |
| <span data-ttu-id="090f0-4075">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4075">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4077">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4077">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4079">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4079">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4081">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4081">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4082">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4082">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4083">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4083">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4085">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4087">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4087">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4089">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4089">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4091">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4091">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4093">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4093">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-4094">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4094">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4095">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4095">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4096">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4096">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4097">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4097">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4098">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4098">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4100">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4100">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-4101">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4101">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4103">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4103">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4104">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4104">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4105">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4105">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4106">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4106">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4107">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4107">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4108">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4108">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4109">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4109">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4110">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4110">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4111">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4111">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4112">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4112">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4113">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4113">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4114">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4114">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4115">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4115">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4116">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4116">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4117">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4117">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4119">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4119">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4121">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4121">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4123">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4123">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4125">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4125">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-4126">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4126">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4128">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4128">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4129">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4129">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4131">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4131">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4132">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4132">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4133">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4133">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4134">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4134">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4136">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4136">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="090f0-4137">DXGI_FORMAT_R8 \_ Typen losen<sup>PCs</sup> (60)</span><span class="sxs-lookup"><span data-stu-id="090f0-4137">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="090f0-4138">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4138">Target</span></span> | <span data-ttu-id="090f0-4139">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4139">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4140">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4140">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4141">8</span><span class="sxs-lookup"><span data-stu-id="090f0-4141">8</span></span> |
| <span data-ttu-id="090f0-4142">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4142">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4144">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4144">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4145">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4145">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4146">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4146">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4147">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4147">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4148">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4148">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4150">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4152">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4152">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4154">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4156">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4156">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-4157">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4157">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-4158">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4158">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4159">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4159">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4160">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4160">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4161">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4161">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4162">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4162">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4164">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4164">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-4165">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4165">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4166">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4166">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4167">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4167">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4168">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4168">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4169">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4169">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4170">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4170">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4171">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4171">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4172">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4172">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4173">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4173">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4174">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4174">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4175">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4175">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4176">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4176">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4177">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4177">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4178">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4178">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4179">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4179">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4180">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4180">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4182">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4182">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4183">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4183">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4184">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4184">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-4185">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4185">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-4186">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4186">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-4187">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4187">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4188">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4188">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4190">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4190">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4191">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4191">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4192">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4192">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4193">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4193">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4195">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="090f0-4196">DXGI_FORMAT_R8 \_ unorm-Datei-<sup>e</sup> /a (61)</span><span class="sxs-lookup"><span data-stu-id="090f0-4196">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="090f0-4197">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4197">Target</span></span> | <span data-ttu-id="090f0-4198">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4198">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4199">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4200">8</span><span class="sxs-lookup"><span data-stu-id="090f0-4200">8</span></span> |
| <span data-ttu-id="090f0-4201">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4201">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4203">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4203">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4205">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4205">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4207">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4207">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4208">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4208">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4209">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4209">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4211">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4213">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4215">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4215">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4217">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4217">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4219">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4219">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4221">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4221">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4222">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4222">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4223">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4223">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4225">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4226">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4226">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4228">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4228">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4230">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4230">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4232">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4232">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4234">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4234">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4235">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4235">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4236">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4236">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4237">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4237">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4238">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4238">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4239">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4239">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4240">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4240">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4241">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4241">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4242">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4242">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4243">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4243">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4244">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4244">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4245">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4245">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4246">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4246">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4247">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4247">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4249">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4249">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4251">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4251">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4253">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4253">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4255">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4255">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4257">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4257">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4259">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4259">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4260">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4260">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4262">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4262">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4263">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4263">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4264">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4264">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4265">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4265">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4267">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4267">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="090f0-4268">DXGI_FORMAT_R8 \_ uint-<sup>f</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="090f0-4268">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="090f0-4269">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4269">Target</span></span> | <span data-ttu-id="090f0-4270">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4270">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4271">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4271">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4272">8</span><span class="sxs-lookup"><span data-stu-id="090f0-4272">8</span></span> |
| <span data-ttu-id="090f0-4273">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4273">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4275">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4275">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4277">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4277">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4279">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4279">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4280">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4280">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4281">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4281">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4283">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4283">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4285">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4287">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4289">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4289">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4291">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-4292">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4293">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4294">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4294">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4295">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4296">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4296">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4298">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4298">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-4299">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4299">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4301">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4302">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4302">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4304">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4305">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4306">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4307">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4307">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4308">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4309">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4310">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4311">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4312">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4312">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4313">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4314">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4315">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4316">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4316">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4318">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4318">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4320">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4320">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4322">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4322">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4324">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4324">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-4325">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4325">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4327">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4327">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4328">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4328">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4330">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4331">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4332">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4333">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4333">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4335">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4335">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="090f0-4336">DXGI_FORMAT_R8 \_ snorm<sup></sup> -snorm (63)</span><span class="sxs-lookup"><span data-stu-id="090f0-4336">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="090f0-4337">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4337">Target</span></span> | <span data-ttu-id="090f0-4338">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4338">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4339">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4339">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4340">8</span><span class="sxs-lookup"><span data-stu-id="090f0-4340">8</span></span> |
| <span data-ttu-id="090f0-4341">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4341">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4343">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4343">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4345">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4345">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4347">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4348">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4349">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4351">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4351">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4353">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4355">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4355">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4357">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4357">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4359">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4359">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4361">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4361">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4362">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4362">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4363">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4363">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4365">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4365">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4366">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4366">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4368">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4368">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4370">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4372">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4372">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4374">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4375">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4376">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4377">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4378">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4379">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4380">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4381">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4382">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4383">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4383">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4384">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4385">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4386">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4387">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4387">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4389">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4389">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4391">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4391">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4393">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4393">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4395">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4395">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4397">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4397">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4399">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4399">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4400">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4400">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4402">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4402">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4403">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4403">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4404">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4404">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4405">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4405">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4407">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4407">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="090f0-4408">DXGI_FORMAT_R8 \_ Sint<sup></sup> -Werte (64)</span><span class="sxs-lookup"><span data-stu-id="090f0-4408">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="090f0-4409">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4409">Target</span></span> | <span data-ttu-id="090f0-4410">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4410">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4411">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4411">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4412">8</span><span class="sxs-lookup"><span data-stu-id="090f0-4412">8</span></span> |
| <span data-ttu-id="090f0-4413">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4413">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4415">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4415">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4417">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4417">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4419">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4419">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4420">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4420">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4421">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4421">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4423">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4425">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4427">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4429">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4429">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4431">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4431">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-4432">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4432">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4433">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4433">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4434">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4434">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4435">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4435">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4436">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4436">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4438">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4438">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-4439">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4439">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4441">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4441">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4442">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4442">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4443">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4443">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4444">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4444">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4445">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4445">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4446">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4446">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4447">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4447">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4448">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4448">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4449">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4449">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4450">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4450">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4451">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4451">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4452">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4452">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4453">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4453">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4454">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4454">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4455">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4455">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4457">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4457">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4459">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4459">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4461">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4461">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4463">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4463">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-4464">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4464">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4466">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4466">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4467">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4467">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4469">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4469">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4470">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4470">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4471">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4471">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4472">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4472">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4474">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4474">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="090f0-4475">DXGI_FORMAT_A8 \_ unorm<sup></sup> -Fehler (65)</span><span class="sxs-lookup"><span data-stu-id="090f0-4475">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="090f0-4476">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4476">Target</span></span> | <span data-ttu-id="090f0-4477">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4477">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4478">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4478">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4479">8</span><span class="sxs-lookup"><span data-stu-id="090f0-4479">8</span></span> |
| <span data-ttu-id="090f0-4480">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4480">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4482">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4482">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4483">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4483">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4484">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4484">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4485">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4485">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4486">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4486">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4488">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4488">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4490">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4492">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4492">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4494">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4494">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4496">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4496">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4498">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4498">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4499">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4499">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4500">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4500">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4501">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4501">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4502">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4502">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4504">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4504">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4506">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4506">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4508">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4508">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4510">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4510">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4511">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4511">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4512">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4512">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4513">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4513">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4514">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4514">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4515">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4515">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4516">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4516">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4517">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4517">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4518">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4518">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4519">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4519">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4520">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4520">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4521">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4521">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4522">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4522">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4523">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4523">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4525">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4525">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4527">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4527">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4529">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4529">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-4531">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4531">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4533">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4533">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4535">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4536">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-4537">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4538">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4539">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4540">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4540">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4542">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="090f0-4543">DXGI_FORMAT_R9G9B9E5 \_ sharede XP-<sup>LNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="090f0-4543">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="090f0-4544">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4544">Target</span></span> | <span data-ttu-id="090f0-4545">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4546">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4547">32</span><span class="sxs-lookup"><span data-stu-id="090f0-4547">32</span></span> |
| <span data-ttu-id="090f0-4548">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4548">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4550">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4551">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4552">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4553">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4554">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4556">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4558">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4558">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4560">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4560">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4562">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4562">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4564">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4564">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4566">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4567">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4568">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4569">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4570">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4570">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4572">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4572">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-4573">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4573">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4574">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4574">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4575">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4575">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4576">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4576">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4577">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4577">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4578">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4578">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4579">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4579">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4580">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4580">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4581">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4581">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4582">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4582">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4583">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4583">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4584">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4584">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4585">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4585">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4586">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4586">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4587">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4587">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4588">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4588">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4590">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4590">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4591">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4591">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4592">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4592">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-4593">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4593">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-4594">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4594">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-4595">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4595">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4596">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4596">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-4597">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4597">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4598">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4598">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4599">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4599">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4600">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4600">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-4601">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4601">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="090f0-4602">DXGI_FORMAT_R8G8 \_ B8G8 \_ unorm<sup></sup> -Fehler (68)</span><span class="sxs-lookup"><span data-stu-id="090f0-4602">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="090f0-4603">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4603">Target</span></span> | <span data-ttu-id="090f0-4604">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4604">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4605">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4605">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4606">16</span><span class="sxs-lookup"><span data-stu-id="090f0-4606">16</span></span> |
| <span data-ttu-id="090f0-4607">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4607">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4609">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4609">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4610">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4610">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4611">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4611">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4612">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4612">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4613">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4613">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4615">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4617">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4617">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4619">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4619">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4621">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4621">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4623">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4623">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4625">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4625">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4626">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4626">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4627">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4627">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4628">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4628">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4629">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4629">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4631">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4631">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-4632">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4632">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4633">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4633">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4634">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4634">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4635">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4635">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4636">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4636">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4637">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4637">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4638">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4638">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4639">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4639">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4640">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4640">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4641">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4641">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4642">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4642">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4643">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4643">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4644">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4644">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4645">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4645">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4646">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4646">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4647">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4647">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4649">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4649">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4650">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4650">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4651">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4651">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-4652">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-4653">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4653">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-4654">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4654">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4655">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4655">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-4656">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4656">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4657">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4657">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4658">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4658">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4659">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4659">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-4660">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4660">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="090f0-4661">DXGI_FORMAT_G8R8 \_ G8B8 \_ unorm<sup></sup> -Fehler (69)</span><span class="sxs-lookup"><span data-stu-id="090f0-4661">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="090f0-4662">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4662">Target</span></span> | <span data-ttu-id="090f0-4663">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4663">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4664">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4664">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4665">16</span><span class="sxs-lookup"><span data-stu-id="090f0-4665">16</span></span> |
| <span data-ttu-id="090f0-4666">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4666">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4668">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4668">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4669">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4669">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4670">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4670">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4671">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4671">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4672">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4672">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4674">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4674">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4676">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4678">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4678">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4680">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4680">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4682">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4682">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4684">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4685">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4686">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4686">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4687">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4688">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4688">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4690">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-4691">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4691">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4692">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4693">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4694">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4695">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4696">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4697">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4697">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4698">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4699">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4700">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4701">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4702">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4703">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4704">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4705">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4706">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4706">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4708">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4709">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4710">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-4711">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-4712">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4712">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-4713">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4714">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4714">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-4715">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4715">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4716">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4716">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4717">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4717">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4718">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4718">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-4719">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4719">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="090f0-4720">DXGI_FORMAT_BC1 \_ typloses<sup>PCC</sup> (70)</span><span class="sxs-lookup"><span data-stu-id="090f0-4720">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="090f0-4721">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4721">Target</span></span> | <span data-ttu-id="090f0-4722">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4722">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4723">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4723">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4724">4</span><span class="sxs-lookup"><span data-stu-id="090f0-4724">4</span></span> |
| <span data-ttu-id="090f0-4725">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4725">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4727">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4727">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4728">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4728">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4729">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4729">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4730">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4730">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4731">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4731">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-4732">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4732">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4734">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4734">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4736">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4736">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4738">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4738">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-4739">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4739">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-4740">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4740">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4741">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4741">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4742">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4742">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4743">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4743">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4744">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4744">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4746">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4746">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-4747">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4747">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4748">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4748">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4749">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4749">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4750">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4750">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4751">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4751">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4752">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4752">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4753">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4753">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4754">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4754">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4755">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4755">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4756">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4756">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4757">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4757">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4758">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4758">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4759">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4759">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4760">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4760">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4761">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4761">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4762">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4762">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4764">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4764">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4765">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4765">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4766">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4766">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-4767">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4767">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-4768">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4768">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-4769">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4769">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4770">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4770">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4772">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4772">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4773">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4773">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4774">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4774">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4775">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4775">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4777">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4777">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="090f0-4778">DXGI_FORMAT_BC1 \_ unorm<sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="090f0-4778">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="090f0-4779">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4779">Target</span></span> | <span data-ttu-id="090f0-4780">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4780">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4781">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4781">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4782">4</span><span class="sxs-lookup"><span data-stu-id="090f0-4782">4</span></span> |
| <span data-ttu-id="090f0-4783">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4783">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4785">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4785">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4786">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4786">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4787">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4787">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4788">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4788">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4789">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4789">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-4790">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4790">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4792">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4792">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4794">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4794">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4796">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4796">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4798">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4798">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4800">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4800">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4801">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4801">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4802">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4802">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4803">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4803">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4804">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4804">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4806">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-4807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4807">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4808">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4809">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4810">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4811">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4812">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4813">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4813">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4814">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4815">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4816">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4817">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4818">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4818">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4819">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4820">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4821">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4822">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4822">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4824">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4824">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4825">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4825">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4826">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4826">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-4827">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4827">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-4828">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4828">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-4829">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4829">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4830">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4830">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4832">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4832">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4833">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4833">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4834">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4834">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4835">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4835">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4837">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="090f0-4838">DXGI_FORMAT_BC1 \_ unorm \_ sRGB<sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="090f0-4838">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="090f0-4839">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4839">Target</span></span> | <span data-ttu-id="090f0-4840">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4840">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4841">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4842">4</span><span class="sxs-lookup"><span data-stu-id="090f0-4842">4</span></span> |
| <span data-ttu-id="090f0-4843">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4843">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4845">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4845">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4846">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4846">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4847">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4847">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4848">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4848">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4849">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4849">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-4850">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4850">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4852">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4852">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4854">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4854">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4856">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4856">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4858">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4858">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4860">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4860">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4861">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4861">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4862">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4862">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4863">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4863">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4864">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4864">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4866">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-4867">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4867">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4868">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4869">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4870">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4871">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4872">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4873">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4873">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4874">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4875">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4876">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4877">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4878">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4879">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4880">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4881">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4882">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4882">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4884">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4885">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4886">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-4887">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-4888">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4888">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-4889">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4890">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4890">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4892">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4892">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4893">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4893">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4894">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4895">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4895">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4897">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4897">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="090f0-4898">DXGI_FORMAT_BC2 \_ typloses<sup>PCC</sup> (73)</span><span class="sxs-lookup"><span data-stu-id="090f0-4898">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="090f0-4899">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4899">Target</span></span> | <span data-ttu-id="090f0-4900">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4900">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4901">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4901">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4902">8</span><span class="sxs-lookup"><span data-stu-id="090f0-4902">8</span></span> |
| <span data-ttu-id="090f0-4903">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4903">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4905">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4905">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4906">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4906">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4907">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4907">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4908">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4908">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4909">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4909">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-4910">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4910">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4912">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4912">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4914">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4914">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4916">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4916">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-4917">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4917">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-4918">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4918">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4919">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4919">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4920">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4920">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4921">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4921">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4922">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4922">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4924">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4924">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-4925">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4925">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4926">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4926">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4927">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4927">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4928">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4928">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4929">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4929">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4930">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4930">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4931">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4931">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4932">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4932">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4933">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4933">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4934">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4934">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4935">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4935">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4936">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4936">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4937">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4937">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4938">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4938">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4939">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4939">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4940">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-4940">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4942">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4942">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4943">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4943">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4944">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-4944">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-4945">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-4945">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-4946">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4946">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-4947">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-4947">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-4948">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-4948">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4950">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-4950">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-4951">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4951">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-4952">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-4952">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-4953">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4953">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4955">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-4955">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="090f0-4956">DXGI_FORMAT_BC2 \_ unorm<sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="090f0-4956">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="090f0-4957">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4957">Target</span></span> | <span data-ttu-id="090f0-4958">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-4958">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-4959">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-4959">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-4960">8</span><span class="sxs-lookup"><span data-stu-id="090f0-4960">8</span></span> |
| <span data-ttu-id="090f0-4961">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-4961">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4963">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4963">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4964">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-4964">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4965">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-4965">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4966">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-4966">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-4967">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-4967">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-4968">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-4968">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4970">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-4970">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-4972">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4974">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-4974">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4976">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4976">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4978">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4978">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-4979">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-4979">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-4980">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-4980">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-4981">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-4981">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-4982">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4982">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-4984">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-4984">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-4985">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4985">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4986">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-4986">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-4987">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-4987">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-4988">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-4988">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-4989">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4989">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4990">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-4990">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-4991">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-4991">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-4992">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-4992">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-4993">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-4993">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-4994">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-4994">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-4995">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-4995">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-4996">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-4996">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-4997">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-4997">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-4998">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-4998">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-4999">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-4999">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5000">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5000">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5002">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5002">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5003">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5003">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5004">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5004">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5005">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5006">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5006">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5007">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5007">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5008">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5008">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5010">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5011">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5012">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5013">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5013">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5015">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5015">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="090f0-5016">DXGI_FORMAT_BC2 \_ unorm \_ sRGB<sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="090f0-5016">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="090f0-5017">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5017">Target</span></span> | <span data-ttu-id="090f0-5018">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5018">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5019">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5019">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5020">8</span><span class="sxs-lookup"><span data-stu-id="090f0-5020">8</span></span> |
| <span data-ttu-id="090f0-5021">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5021">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5023">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5023">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5024">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5024">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5025">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5025">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5026">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5026">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5027">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5027">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-5028">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5028">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5030">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5032">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5032">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5034">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5034">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5036">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5036">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5038">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5038">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5039">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5039">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5040">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5040">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5041">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5041">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5042">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5042">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5044">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5044">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-5045">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5045">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5046">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5046">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5047">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5047">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5048">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5048">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5049">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5049">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5050">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5050">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5051">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5051">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5052">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5052">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5053">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5053">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5054">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5054">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5055">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5055">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5056">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5056">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5057">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5057">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5058">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5058">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5059">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5059">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5060">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5060">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5062">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5062">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5063">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5063">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5064">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5064">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5065">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5066">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5067">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5068">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5068">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5070">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5070">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5071">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5071">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5072">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5072">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5073">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5073">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5075">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="090f0-5076">DXGI_FORMAT_BC3 \_ typloses<sup>PCC</sup> (76)</span><span class="sxs-lookup"><span data-stu-id="090f0-5076">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="090f0-5077">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5077">Target</span></span> | <span data-ttu-id="090f0-5078">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5078">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5079">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5080">8</span><span class="sxs-lookup"><span data-stu-id="090f0-5080">8</span></span> |
| <span data-ttu-id="090f0-5081">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5081">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5083">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5083">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5084">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5085">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5086">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5087">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-5088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5088">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5090">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5090">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5092">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5092">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5094">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5094">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-5095">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5095">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-5096">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5096">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5097">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5097">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5098">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5098">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5099">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5099">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5100">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5100">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5102">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5102">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-5103">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5103">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5104">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5104">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5105">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5105">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5106">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5106">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5107">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5107">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5108">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5108">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5109">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5109">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5110">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5110">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5111">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5111">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5112">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5112">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5113">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5113">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5114">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5114">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5115">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5115">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5116">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5116">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5117">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5117">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5118">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5118">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5120">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5120">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5121">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5121">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5122">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5122">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5123">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5123">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5124">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5124">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5125">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5125">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5126">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5126">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5128">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5128">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5129">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5129">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5130">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5130">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5131">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5131">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5133">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5133">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="090f0-5134">DXGI_FORMAT_BC3 \_ unorm<sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="090f0-5134">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="090f0-5135">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5135">Target</span></span> | <span data-ttu-id="090f0-5136">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5136">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5137">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5137">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5138">8</span><span class="sxs-lookup"><span data-stu-id="090f0-5138">8</span></span> |
| <span data-ttu-id="090f0-5139">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5139">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5141">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5141">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5142">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5142">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5143">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5143">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5144">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5144">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5145">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5145">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-5146">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5146">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5148">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5148">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5150">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5150">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5152">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5152">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5154">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5154">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5156">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5156">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5157">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5157">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5158">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5158">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5159">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5159">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5160">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5160">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5162">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-5163">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5163">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5164">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5165">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5166">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5167">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5168">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5169">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5169">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5170">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5171">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5172">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5173">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5174">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5175">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5176">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5177">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5178">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5178">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5180">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5180">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5181">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5181">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5182">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5182">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5183">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5183">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5184">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5184">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5185">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5185">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5186">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5186">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5188">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5188">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5189">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5189">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5190">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5190">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5191">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5191">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5193">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5193">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="090f0-5194">DXGI_FORMAT_BC3 \_ unorm \_ sRGB<sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="090f0-5194">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="090f0-5195">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5195">Target</span></span> | <span data-ttu-id="090f0-5196">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5196">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5197">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5197">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5198">8</span><span class="sxs-lookup"><span data-stu-id="090f0-5198">8</span></span> |
| <span data-ttu-id="090f0-5199">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5199">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5201">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5201">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5202">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5202">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5203">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5203">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5204">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5204">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5205">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5205">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-5206">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5206">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5208">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5210">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5210">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5212">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5212">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5214">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5214">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5216">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5216">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5217">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5217">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5218">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5218">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5219">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5219">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5220">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5220">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5222">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-5223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5224">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5225">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5226">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5227">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5228">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5229">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5230">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5231">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5232">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5233">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5234">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5234">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5235">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5236">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5237">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5238">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5238">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5240">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5241">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5242">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5243">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5244">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5245">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5246">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5246">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5248">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5248">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5249">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5249">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5250">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5250">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5251">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5251">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5253">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5253">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="090f0-5254">DXGI_FORMAT_BC4 \_ typloses<sup>PCC</sup> (79)</span><span class="sxs-lookup"><span data-stu-id="090f0-5254">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="090f0-5255">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5255">Target</span></span> | <span data-ttu-id="090f0-5256">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5256">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5257">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5257">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5258">4</span><span class="sxs-lookup"><span data-stu-id="090f0-5258">4</span></span> |
| <span data-ttu-id="090f0-5259">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5259">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5261">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5261">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5262">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5262">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5263">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5264">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5265">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-5266">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5266">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5268">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5268">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5270">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5272">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5272">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-5273">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5273">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-5274">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5274">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5275">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5275">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5276">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5276">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5277">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5277">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5278">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5278">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5280">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5280">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-5281">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5281">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5282">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5282">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5283">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5283">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5284">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5284">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5285">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5285">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5286">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5286">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5287">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5287">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5288">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5288">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5289">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5289">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5290">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5290">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5291">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5291">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5292">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5292">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5293">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5293">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5294">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5294">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5295">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5295">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5296">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5296">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5298">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5298">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5299">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5299">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5300">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5300">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5301">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5302">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5302">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5303">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5303">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5304">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5304">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5306">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5306">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5307">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5307">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5308">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5308">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5309">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-5310">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="090f0-5311">DXGI_FORMAT_BC4 \_ unorm<sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="090f0-5311">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="090f0-5312">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5312">Target</span></span> | <span data-ttu-id="090f0-5313">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5314">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5315">4</span><span class="sxs-lookup"><span data-stu-id="090f0-5315">4</span></span> |
| <span data-ttu-id="090f0-5316">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5316">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5318">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5318">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5319">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5320">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5321">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5323">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5325">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5327">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5329">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5329">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5331">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5331">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5333">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5333">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5334">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5334">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5335">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5335">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5336">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5336">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5337">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5337">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5339">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5341">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5342">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5343">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5344">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5345">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5346">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5347">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5348">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5349">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5350">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5352">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5353">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5354">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5355">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5355">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5357">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5358">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5359">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5360">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5361">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5362">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5363">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5363">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5365">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5365">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5366">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5366">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5367">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5367">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5368">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5368">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-5369">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5369">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="090f0-5370">DXGI_FORMAT_BC4 \_ snorm<sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="090f0-5370">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="090f0-5371">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5371">Target</span></span> | <span data-ttu-id="090f0-5372">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5372">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5373">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5373">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5374">4</span><span class="sxs-lookup"><span data-stu-id="090f0-5374">4</span></span> |
| <span data-ttu-id="090f0-5375">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5375">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5377">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5377">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5378">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5378">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5379">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5379">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5380">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5380">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5381">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5381">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-5382">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5382">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5384">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5384">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5386">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5388">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5388">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5390">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5390">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5392">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5392">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5393">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5393">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5394">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5394">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5395">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5395">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5396">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5396">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5398">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-5399">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5399">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5400">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5400">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5401">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5401">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5402">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5402">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5403">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5403">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5404">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5404">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5405">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5405">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5406">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5406">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5407">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5407">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5408">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5408">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5409">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5409">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5410">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5410">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5411">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5411">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5412">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5412">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5413">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5413">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5414">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5414">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5416">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5416">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5417">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5417">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5418">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5418">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5419">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5419">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5420">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5420">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5421">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5421">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5422">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5422">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5424">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5424">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5425">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5425">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5426">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5426">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5427">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5427">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-5428">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5428">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="090f0-5429">DXGI_FORMAT_BC5 \_ typloses<sup>PCC</sup> (82)</span><span class="sxs-lookup"><span data-stu-id="090f0-5429">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="090f0-5430">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5430">Target</span></span> | <span data-ttu-id="090f0-5431">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5431">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5432">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5432">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5433">8</span><span class="sxs-lookup"><span data-stu-id="090f0-5433">8</span></span> |
| <span data-ttu-id="090f0-5434">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5434">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5436">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5436">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5437">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5437">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5438">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5438">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5439">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5439">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5440">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5440">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-5441">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5441">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5443">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5443">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5445">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5445">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5447">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5447">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-5448">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5448">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-5449">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5449">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5450">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5450">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5451">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5451">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5452">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5452">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5453">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5453">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5455">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5455">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-5456">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5456">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5457">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5457">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5458">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5458">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5459">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5459">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5460">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5460">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5461">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5461">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5462">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5462">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5463">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5463">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5464">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5464">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5465">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5465">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5466">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5466">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5467">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5467">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5468">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5468">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5469">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5469">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5470">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5470">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5471">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5471">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5473">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5473">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5474">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5474">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5475">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5475">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5476">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5476">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5477">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5477">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5478">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5479">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5479">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5481">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5482">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5483">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5484">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5484">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-5485">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="090f0-5486">DXGI_FORMAT_BC5 \_ unorm<sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="090f0-5486">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="090f0-5487">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5487">Target</span></span> | <span data-ttu-id="090f0-5488">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5488">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5489">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5490">8</span><span class="sxs-lookup"><span data-stu-id="090f0-5490">8</span></span> |
| <span data-ttu-id="090f0-5491">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5491">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5493">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5493">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5494">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5495">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5496">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5497">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-5498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5498">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5500">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5500">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5502">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5502">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5504">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5504">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5506">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5506">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5508">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5509">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5510">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5510">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5511">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5512">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5512">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5514">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-5515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5515">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5516">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5517">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5518">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5519">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5520">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5521">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5521">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5522">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5523">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5524">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5525">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5526">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5526">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5527">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5528">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5529">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5530">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5530">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5532">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5532">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5533">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5533">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5534">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5534">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5535">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5535">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5536">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5536">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5537">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5537">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5538">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5538">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5540">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5541">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5542">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5543">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5543">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-5544">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="090f0-5545">DXGI_FORMAT_BC5 \_ snorm<sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="090f0-5545">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="090f0-5546">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5546">Target</span></span> | <span data-ttu-id="090f0-5547">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5547">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5548">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5549">8</span><span class="sxs-lookup"><span data-stu-id="090f0-5549">8</span></span> |
| <span data-ttu-id="090f0-5550">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5550">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5552">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5552">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5553">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5553">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5554">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5554">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5555">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5555">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5556">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5556">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-5557">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5557">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5559">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5559">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5561">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5561">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5563">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5563">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5565">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5565">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5567">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5567">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5568">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5568">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5569">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5569">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5570">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5570">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5571">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5571">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5573">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5573">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-5574">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5574">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5575">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5575">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5576">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5577">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5578">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5579">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5580">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5580">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5581">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5582">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5583">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5584">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5585">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5585">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5586">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5587">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5588">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5589">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5589">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5591">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5591">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5592">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5592">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5593">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5593">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5594">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5594">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5595">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5595">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5596">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5596">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5597">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5597">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5599">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5600">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5601">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5602">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5602">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-5603">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="090f0-5604">DXGI_FORMAT_B5G6R5 \_ unorm<sup></sup> -Fehler (85)</span><span class="sxs-lookup"><span data-stu-id="090f0-5604">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="090f0-5605">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5605">Target</span></span> | <span data-ttu-id="090f0-5606">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5606">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5607">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5608">16</span><span class="sxs-lookup"><span data-stu-id="090f0-5608">16</span></span> |
| <span data-ttu-id="090f0-5609">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5609">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5611">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5611">Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5613">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5613">Input Assembler Vertex Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5615">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5615">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5616">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5616">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5617">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5617">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5619">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5621">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5623">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5623">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5625">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5625">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5627">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5627">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5629">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5629">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5630">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5630">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5631">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5631">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5632">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5632">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5633">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5633">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5635">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5635">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5637">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5637">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5639">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5639">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5641">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5641">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5642">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5642">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5643">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5643">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5644">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5644">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5645">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5645">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5646">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5646">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5647">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5647">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5648">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5648">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5649">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5649">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5650">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5650">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5651">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5651">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5652">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5652">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5653">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5653">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5654">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5654">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5656">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5656">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5658">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5658">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5660">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5660">Other Multisample Count RT</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5662">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5662">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5664">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5664">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5666">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5666">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5667">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5667">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-5668">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5669">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5670">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5671">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5671">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-5672">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5672">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="090f0-5673">DXGI_FORMAT_B5G5R5A1 \_ unorm<sup></sup> -Fehler (86)</span><span class="sxs-lookup"><span data-stu-id="090f0-5673">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="090f0-5674">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5674">Target</span></span> | <span data-ttu-id="090f0-5675">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5675">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5676">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5676">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5677">16</span><span class="sxs-lookup"><span data-stu-id="090f0-5677">16</span></span> |
| <span data-ttu-id="090f0-5678">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5678">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5680">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5680">Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5682">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5682">Input Assembler Vertex Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5684">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5684">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5685">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5685">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5686">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5686">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5688">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5688">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5690">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5690">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5692">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5692">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5694">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5694">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5696">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5696">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5698">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5698">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5699">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5699">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5700">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5700">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5701">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5701">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5702">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5702">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5704">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5704">Mipmap Auto-Generation</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5706">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5706">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5708">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5708">Blendable RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5710">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5710">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5711">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5711">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5712">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5712">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5713">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5713">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5714">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5714">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5715">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5715">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5716">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5716">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5717">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5717">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5718">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5718">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5719">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5719">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5720">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5720">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5721">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5721">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5722">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5722">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5723">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5723">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5725">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5725">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5727">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5727">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5729">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5729">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5731">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5731">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5733">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5733">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5735">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5735">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5736">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5736">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-5737">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5737">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5738">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5738">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5739">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5739">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5740">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5740">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-5741">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5741">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="090f0-5742">DXGI_FORMAT_B8G8R8A8 \_ Typen losen<sup>PCs</sup> (90)</span><span class="sxs-lookup"><span data-stu-id="090f0-5742">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="090f0-5743">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5743">Target</span></span> | <span data-ttu-id="090f0-5744">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5744">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5745">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5745">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5746">32</span><span class="sxs-lookup"><span data-stu-id="090f0-5746">32</span></span> |
| <span data-ttu-id="090f0-5747">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5747">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5749">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5749">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5750">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5750">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5751">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5751">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5752">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5752">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5753">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5753">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5755">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5755">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5757">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5759">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5759">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5761">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5761">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-5762">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5762">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-5763">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5763">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5764">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5764">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5765">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5765">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5766">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5766">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5767">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5767">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5769">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5769">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-5770">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5770">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5771">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5771">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5772">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5772">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5773">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5773">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5774">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5774">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5775">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5775">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5776">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5776">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5777">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5777">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5778">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5778">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5779">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5779">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5780">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5780">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5781">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5781">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5782">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5782">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5783">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5783">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5784">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5784">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5785">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5785">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5787">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5787">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5788">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5788">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5789">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5789">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5790">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5790">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5791">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5791">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5792">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5792">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5793">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5793">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5795">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5795">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5796">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5796">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-5797">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5797">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-5798">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5798">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5800">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="090f0-5801">DXGI_FORMAT_B8G8R8A8 \_ unorm-Datei-<sup>e</sup> /a (87)</span><span class="sxs-lookup"><span data-stu-id="090f0-5801">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="090f0-5802">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5802">Target</span></span> | <span data-ttu-id="090f0-5803">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5803">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5804">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5805">32</span><span class="sxs-lookup"><span data-stu-id="090f0-5805">32</span></span> |
| <span data-ttu-id="090f0-5806">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5806">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5808">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5808">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5810">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5810">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5812">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5812">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5813">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5813">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5814">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5814">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5816">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5816">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5818">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5818">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5820">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5820">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5822">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5822">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5824">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5824">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5826">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5826">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5827">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5827">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5828">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5828">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5829">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5829">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5830">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5830">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5832">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5832">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5834">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5834">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5836">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5836">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5838">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5839">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5840">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5841">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5842">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5843">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5844">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5845">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5846">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5847">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5847">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5848">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5849">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5850">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5851">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5851">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5853">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5853">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5855">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5855">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5857">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5857">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5859">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5859">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5861">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5861">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5863">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5863">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5865">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5865">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5867">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5867">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5868">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5868">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5870">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5870">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5872">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5872">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5874">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5874">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="090f0-5875">DXGI_FORMAT_B8G8R8A8 \_ unorm \_ sRGB-Datei-<sup>e</sup> /a (91)</span><span class="sxs-lookup"><span data-stu-id="090f0-5875">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="090f0-5876">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5876">Target</span></span> | <span data-ttu-id="090f0-5877">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5877">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5878">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5878">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5879">32</span><span class="sxs-lookup"><span data-stu-id="090f0-5879">32</span></span> |
| <span data-ttu-id="090f0-5880">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5880">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5882">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5882">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5883">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5883">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5884">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5884">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5885">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5885">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5886">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5886">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5888">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5888">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5890">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5890">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5892">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5894">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5894">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5896">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5896">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5898">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5898">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5899">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5899">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5900">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5900">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5901">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5901">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5902">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5902">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5904">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5904">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5906">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5906">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5908">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5908">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5910">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5910">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5911">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5911">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5912">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5912">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5913">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5913">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5914">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5914">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5915">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5915">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5916">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5916">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5917">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5917">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5918">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5918">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5919">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5919">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5920">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5920">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5921">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5921">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5922">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5922">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5923">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5923">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5925">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5925">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5927">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5927">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5929">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5929">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5931">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5931">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5933">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5933">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5935">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5935">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5937">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5937">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5939">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-5939">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-5940">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5940">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5942">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-5942">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-5944">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5944">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5946">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-5946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="090f0-5947">DXGI_FORMAT_B8G8R8X8 \_ Typen losen<sup>PCs</sup> (92)</span><span class="sxs-lookup"><span data-stu-id="090f0-5947">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="090f0-5948">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5948">Target</span></span> | <span data-ttu-id="090f0-5949">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-5949">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-5950">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-5950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-5951">32</span><span class="sxs-lookup"><span data-stu-id="090f0-5951">32</span></span> |
| <span data-ttu-id="090f0-5952">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-5952">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5954">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5954">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5955">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-5955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5956">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-5956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5957">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-5957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-5958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-5958">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-5960">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-5962">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-5964">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5966">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-5966">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-5967">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-5968">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-5969">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-5969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-5970">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-5970">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-5971">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-5971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-5972">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5972">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5974">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-5974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-5975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5975">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5976">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5977">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-5977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-5978">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-5978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-5979">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5980">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-5980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-5981">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-5981">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-5982">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-5982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-5983">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-5984">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-5984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-5985">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-5985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-5986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-5986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-5987">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-5987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-5988">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-5988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5989">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-5989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-5990">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-5990">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-5992">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5993">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-5993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-5994">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-5994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-5995">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-5995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-5996">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-5996">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-5997">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-5997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-5998">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-5998">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6000">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-6001">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-6002">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-6003">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6003">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6005">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="090f0-6006">DXGI_FORMAT_B8G8R8X8 \_ unorm-Datei-<sup>e</sup> /a (88)</span><span class="sxs-lookup"><span data-stu-id="090f0-6006">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="090f0-6007">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6007">Target</span></span> | <span data-ttu-id="090f0-6008">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6008">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6009">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6010">32</span><span class="sxs-lookup"><span data-stu-id="090f0-6010">32</span></span> |
| <span data-ttu-id="090f0-6011">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6011">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6013">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6013">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6015">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6015">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6017">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6018">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6019">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6021">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6023">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6025">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6027">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6027">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6029">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6029">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6031">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6032">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6033">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6033">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-6034">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6035">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6035">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6037">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6037">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6039">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6041">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6041">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6043">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6044">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6045">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6046">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6047">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6047">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6048">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6049">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6050">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6051">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6053">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6054">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6055">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6056">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6056">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6058">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6058">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6060">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6060">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6062">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6062">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6064">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6064">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6066">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6066">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6068">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6068">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6069">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6069">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6071">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-6072">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6072">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6074">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6074">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6076">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6076">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6078">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6078">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="090f0-6079">DXGI_FORMAT_B8G8R8X8 \_ unorm \_ sRGB-Datei-<sup>e</sup> /a (93)</span><span class="sxs-lookup"><span data-stu-id="090f0-6079">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="090f0-6080">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6080">Target</span></span> | <span data-ttu-id="090f0-6081">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6081">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6082">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6082">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6083">32</span><span class="sxs-lookup"><span data-stu-id="090f0-6083">32</span></span> |
| <span data-ttu-id="090f0-6084">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6084">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6086">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6086">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6087">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6087">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6088">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6088">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6089">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6089">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6090">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6090">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6092">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6092">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6094">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6094">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6096">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6096">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6098">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6098">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6100">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6100">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6102">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6102">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6103">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6103">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6104">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6104">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-6105">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6105">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6106">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6106">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6108">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6108">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6110">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6110">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6112">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6112">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6114">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6115">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6116">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6117">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6118">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6118">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6119">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6120">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6121">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6122">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6123">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6124">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6125">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6126">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6127">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6127">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6129">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6129">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6131">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6131">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6133">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6133">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6135">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6135">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6137">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6137">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6139">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6139">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6140">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6140">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6142">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6142">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-6143">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6143">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-6144">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6144">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-6145">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6145">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6147">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="090f0-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="090f0-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="090f0-6149">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6149">Target</span></span> | <span data-ttu-id="090f0-6150">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6150">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6151">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6152">32</span><span class="sxs-lookup"><span data-stu-id="090f0-6152">32</span></span> |
| <span data-ttu-id="090f0-6153">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6153">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6155">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6155">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6156">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6157">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6158">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6159">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6160">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6162">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6163">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6164">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6164">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6166">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6166">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6168">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6168">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6169">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6169">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6170">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6170">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6172">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6173">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6173">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6175">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6175">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6177">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6177">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6179">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6179">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6181">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6181">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6182">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6182">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6183">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6183">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6184">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6184">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6185">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6185">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6186">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6186">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6187">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6187">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6188">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6188">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6189">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6189">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6190">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6190">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6191">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6191">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6192">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6192">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6193">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6193">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6194">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6194">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6196">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6196">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6197">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6197">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6198">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6198">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6199">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6199">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6200">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6200">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6201">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6201">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6202">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6202">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6203">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6203">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6205">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6205">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6207">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6207">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6209">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6209">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6211">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6211">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="090f0-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="090f0-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="090f0-6213">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6213">Target</span></span> | <span data-ttu-id="090f0-6214">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6214">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6215">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6215">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6216">32</span><span class="sxs-lookup"><span data-stu-id="090f0-6216">32</span></span> |
| <span data-ttu-id="090f0-6217">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6217">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6219">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6219">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6220">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6220">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6221">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6221">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6222">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6222">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6223">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6223">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6224">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6224">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6226">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6226">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6227">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6227">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6228">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6228">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6230">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6230">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6232">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6232">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6233">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6233">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6234">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6234">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6236">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6236">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6237">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6237">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-6238">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6238">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6239">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6239">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6240">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6240">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6241">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6241">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6242">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6242">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6243">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6243">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6244">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6244">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6245">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6245">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6246">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6246">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6247">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6247">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6248">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6248">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6249">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6249">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6250">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6250">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6251">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6251">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6252">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6252">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6253">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6253">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6254">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6254">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6256">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6256">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6257">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6257">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6258">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6258">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6259">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6259">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6260">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6260">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6261">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6261">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6262">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6262">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6263">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6263">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6265">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6265">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6267">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6267">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6269">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6269">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6271">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="090f0-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="090f0-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="090f0-6273">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6273">Target</span></span> | <span data-ttu-id="090f0-6274">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6274">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6275">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6276">64</span><span class="sxs-lookup"><span data-stu-id="090f0-6276">64</span></span> |
| <span data-ttu-id="090f0-6277">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6277">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6279">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6279">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6280">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6281">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6282">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6283">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6284">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6286">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6286">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6287">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6288">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6288">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6290">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6290">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6292">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6293">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6294">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6294">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6296">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6297">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6297">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6299">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6300">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6300">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6301">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6302">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6303">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6304">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6305">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6306">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6306">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6307">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6308">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6309">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6310">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6311">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6312">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6313">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6314">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6315">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6315">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6317">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6318">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6319">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6320">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6321">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6321">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6322">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6323">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6324">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6324">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6326">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6326">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6328">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6328">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6330">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6330">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6332">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6332">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="090f0-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="090f0-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="090f0-6334">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6334">Target</span></span> | <span data-ttu-id="090f0-6335">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6335">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6336">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6336">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6337">8</span><span class="sxs-lookup"><span data-stu-id="090f0-6337">8</span></span> |
| <span data-ttu-id="090f0-6338">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6338">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6340">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6340">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6341">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6341">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6342">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6342">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6343">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6343">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6344">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6344">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6345">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6345">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6347">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6348">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6349">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6349">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6351">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6351">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6353">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6353">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6354">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6354">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6355">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6355">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6357">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6357">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6358">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6358">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-6359">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6359">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6360">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6360">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6362">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6362">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6364">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6364">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6365">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6365">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6366">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6366">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6367">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6367">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6368">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6368">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6369">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6369">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6370">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6370">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6371">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6371">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6372">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6372">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6373">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6373">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6374">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6374">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6375">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6375">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6376">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6376">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6377">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6377">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6379">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6380">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6381">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6382">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6383">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6383">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6384">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6385">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6386">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6386">Video Decoder Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6388">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6388">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6390">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6390">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6392">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6392">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6394">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6394">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="090f0-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="090f0-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="090f0-6396">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6396">Target</span></span> | <span data-ttu-id="090f0-6397">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6397">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6398">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6398">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6399">16</span><span class="sxs-lookup"><span data-stu-id="090f0-6399">16</span></span> |
| <span data-ttu-id="090f0-6400">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6400">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6402">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6402">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6403">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6403">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6404">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6404">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6405">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6405">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6406">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6406">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6407">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6407">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6409">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6409">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6410">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6410">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6411">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6411">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6413">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6413">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6415">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6415">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6416">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6416">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6417">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6417">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6419">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6420">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6420">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-6421">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6422">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6424">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6424">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6426">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6427">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6428">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6429">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6430">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6430">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6431">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6432">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6433">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6434">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6435">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6436">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6437">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6438">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6439">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6439">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6441">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6441">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6442">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6442">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6443">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6443">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6444">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6444">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6445">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6445">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6446">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6446">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6447">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6447">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6448">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6448">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6450">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6450">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6452">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6452">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6454">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6454">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6456">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="090f0-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="090f0-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="090f0-6458">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6458">Target</span></span> | <span data-ttu-id="090f0-6459">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6459">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6460">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6461">16</span><span class="sxs-lookup"><span data-stu-id="090f0-6461">16</span></span> |
| <span data-ttu-id="090f0-6462">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6462">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6464">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6464">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6465">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6466">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6467">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6468">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6469">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6469">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6471">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6471">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6472">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6472">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6473">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6473">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6475">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6475">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6477">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6477">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6478">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6478">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6479">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6479">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6481">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6481">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6482">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6482">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-6483">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6483">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6484">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6484">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6486">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6486">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6488">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6488">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6489">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6489">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6490">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6490">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6491">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6491">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6492">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6492">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6493">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6493">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6494">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6494">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6495">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6495">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6496">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6496">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6497">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6497">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6498">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6498">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6499">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6499">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6500">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6500">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6501">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6501">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6503">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6503">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6504">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6504">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6505">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6505">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6506">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6507">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6507">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6508">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6508">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6509">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6509">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6510">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6510">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6512">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6512">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6514">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6514">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6516">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6516">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6518">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6518">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="090f0-6519">DXGI_FORMAT_420 nicht transparent \_ <sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="090f0-6519">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="090f0-6520">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6520">Target</span></span> | <span data-ttu-id="090f0-6521">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6521">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6522">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6522">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6523">8</span><span class="sxs-lookup"><span data-stu-id="090f0-6523">8</span></span> |
| <span data-ttu-id="090f0-6524">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6524">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6526">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6526">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6527">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6527">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6528">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6529">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6530">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6531">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6531">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6533">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6533">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6534">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6534">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6535">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6535">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-6536">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6536">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-6537">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6537">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6538">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6538">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6539">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6539">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-6540">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6540">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6541">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6541">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-6542">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6542">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6543">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6543">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6544">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6544">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6545">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6545">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6546">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6546">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6547">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6547">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6548">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6548">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6549">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6549">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6550">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6550">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6551">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6551">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6552">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6552">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6553">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6553">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6554">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6554">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6555">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6555">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6556">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6556">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6557">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6557">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6558">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6558">CPU Lockable</span></span> | \- |
| <span data-ttu-id="090f0-6559">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6559">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6560">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6560">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6561">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6561">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6562">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6562">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6563">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6563">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6564">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6564">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6565">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6565">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6566">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6566">Video Decoder Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6568">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6568">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6570">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6570">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6572">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6572">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6574">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6574">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="090f0-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="090f0-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="090f0-6576">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6576">Target</span></span> | <span data-ttu-id="090f0-6577">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6577">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6578">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6578">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6579">16</span><span class="sxs-lookup"><span data-stu-id="090f0-6579">16</span></span> |
| <span data-ttu-id="090f0-6580">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6580">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6582">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6582">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6583">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6583">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6584">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6584">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6585">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6585">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6586">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6586">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6587">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6589">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6590">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6590">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6591">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6591">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6593">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6593">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6595">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6595">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6596">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6596">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6597">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6597">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6599">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6600">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6600">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-6601">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6601">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6602">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6602">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6603">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6603">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6604">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6604">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6605">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6605">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6606">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6606">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6607">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6607">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6608">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6608">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6609">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6609">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6610">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6610">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6611">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6611">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6612">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6612">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6613">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6613">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6614">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6614">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6615">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6615">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6616">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6616">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6617">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6617">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6619">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6619">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6620">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6620">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6621">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6621">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6622">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6622">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6623">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6623">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6624">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6624">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6625">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6625">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6626">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6626">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6628">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6628">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6630">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6630">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6632">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6632">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6634">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6634">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="090f0-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="090f0-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="090f0-6636">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6636">Target</span></span> | <span data-ttu-id="090f0-6637">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6637">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6638">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6638">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6639">32</span><span class="sxs-lookup"><span data-stu-id="090f0-6639">32</span></span> |
| <span data-ttu-id="090f0-6640">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6640">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6642">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6642">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6643">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6643">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6644">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6644">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6645">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6645">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6646">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6646">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6647">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6647">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6649">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6649">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6650">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6650">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6651">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6651">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6653">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6653">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6655">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6655">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6656">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6656">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6657">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6657">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6659">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6659">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6660">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6660">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-6661">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6661">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6662">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6662">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6663">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6663">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6664">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6664">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6665">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6665">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6666">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6666">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6667">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6667">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6668">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6668">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6669">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6669">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6670">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6670">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6671">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6671">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6672">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6672">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6673">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6673">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6674">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6674">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6675">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6675">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6676">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6676">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6677">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6677">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6679">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6679">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6680">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6680">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6681">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6681">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6682">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6682">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6683">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6683">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6684">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6684">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6685">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6685">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6686">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6686">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6688">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6688">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6690">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6690">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6692">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6692">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6694">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="090f0-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="090f0-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="090f0-6696">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6696">Target</span></span> | <span data-ttu-id="090f0-6697">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6697">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6698">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6699">32</span><span class="sxs-lookup"><span data-stu-id="090f0-6699">32</span></span> |
| <span data-ttu-id="090f0-6700">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6700">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6702">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6702">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6703">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6703">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6704">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6705">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6706">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6707">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6707">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6709">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6709">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6710">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6710">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6711">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6711">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6713">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6713">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6715">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6715">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6716">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6716">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6717">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6717">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6719">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6719">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6720">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6720">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-6721">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6721">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6722">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6722">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6723">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6723">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6724">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6724">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6725">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6725">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6726">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6726">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6727">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6727">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6728">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6728">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6729">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6729">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6730">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6730">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6731">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6731">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6732">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6732">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6733">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6733">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6734">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6734">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6735">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6735">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6736">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6736">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6737">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6737">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6739">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6740">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6741">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6742">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6743">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6743">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6744">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6745">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6746">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6746">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6748">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6748">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6750">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6750">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6752">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6752">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6754">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6754">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="090f0-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="090f0-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="090f0-6756">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6756">Target</span></span> | <span data-ttu-id="090f0-6757">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6757">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6758">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6758">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6759">8</span><span class="sxs-lookup"><span data-stu-id="090f0-6759">8</span></span> |
| <span data-ttu-id="090f0-6760">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6760">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6762">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6762">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6763">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6763">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6764">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6764">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6765">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6765">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6766">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6766">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6767">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6769">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6770">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6771">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6771">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6773">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6773">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6775">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6775">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6776">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6776">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6777">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6777">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6779">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6780">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6780">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-6781">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6782">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6782">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6784">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6784">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6786">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6787">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6788">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6789">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6790">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6790">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6791">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6792">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6793">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6794">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6795">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6795">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6796">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6797">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6798">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6799">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6799">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6801">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6801">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6802">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6802">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6803">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6803">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6804">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6805">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6805">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6806">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6806">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6807">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6807">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6808">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6808">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6810">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6810">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6812">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6812">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6814">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6814">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6816">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6816">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="090f0-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="090f0-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="090f0-6818">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6818">Target</span></span> | <span data-ttu-id="090f0-6819">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6819">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6820">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6820">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6821">8</span><span class="sxs-lookup"><span data-stu-id="090f0-6821">8</span></span> |
| <span data-ttu-id="090f0-6822">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6822">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6824">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6824">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6825">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6825">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6826">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6826">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6827">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6827">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6828">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6828">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6829">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6829">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6831">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6831">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6832">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6832">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6833">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6833">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-6834">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6834">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-6835">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6835">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6836">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6836">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6837">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6837">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-6838">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6838">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6839">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6839">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-6840">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6840">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6841">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6841">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6842">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6842">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6843">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6843">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6844">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6844">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6845">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6845">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6846">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6846">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6847">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6847">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6848">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6848">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6849">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6849">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6850">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6850">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6851">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6851">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6852">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6852">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6853">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6853">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6854">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6854">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6855">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6855">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6856">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6856">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6858">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6858">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6859">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6859">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6860">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6860">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6861">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6861">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6862">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6862">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6863">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6863">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6864">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6864">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6865">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6865">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-6866">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6866">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6868">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6868">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-6869">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6869">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-6870">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6870">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="090f0-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="090f0-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="090f0-6872">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6872">Target</span></span> | <span data-ttu-id="090f0-6873">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6873">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6874">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6874">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6875">8</span><span class="sxs-lookup"><span data-stu-id="090f0-6875">8</span></span> |
| <span data-ttu-id="090f0-6876">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6876">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6878">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6878">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6879">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6879">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6880">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6880">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6881">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6881">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6882">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6882">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6883">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6883">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6885">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6885">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6886">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6886">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6887">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6887">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-6888">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6888">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-6889">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6889">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6890">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6890">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6891">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6891">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-6892">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6892">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6893">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6893">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-6894">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6895">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6896">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6897">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6898">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6899">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6900">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6901">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6901">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6902">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6903">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6904">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6905">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6906">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6906">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6907">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6908">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6909">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6910">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6910">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6912">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6913">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6914">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6915">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6916">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6916">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6917">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6918">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6919">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-6920">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6920">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6922">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6922">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-6923">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6923">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-6924">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6924">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="090f0-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="090f0-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="090f0-6926">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6926">Target</span></span> | <span data-ttu-id="090f0-6927">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6927">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6928">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6928">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6929">8</span><span class="sxs-lookup"><span data-stu-id="090f0-6929">8</span></span> |
| <span data-ttu-id="090f0-6930">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6930">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6932">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6932">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6933">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6933">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6934">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6934">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6935">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6935">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6936">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6936">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6937">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6937">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6939">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6939">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6940">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6940">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6941">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6941">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-6942">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6942">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-6943">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6943">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6944">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6944">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6945">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6945">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-6946">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-6946">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-6947">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6947">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-6948">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-6948">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-6949">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6949">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6950">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6951">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-6951">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-6952">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6952">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-6953">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6953">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6954">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-6954">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-6955">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-6955">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-6956">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-6956">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-6957">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6957">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-6958">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-6958">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-6959">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-6959">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-6960">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-6960">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-6961">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-6961">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-6962">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-6962">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6963">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-6963">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-6964">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-6964">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6966">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6966">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6967">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-6967">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-6968">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-6968">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-6969">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-6969">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-6970">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-6970">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-6971">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-6971">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-6972">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-6972">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-6973">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-6973">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-6974">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6974">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6976">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-6976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-6977">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6977">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-6978">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-6978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="090f0-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="090f0-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="090f0-6980">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-6980">Target</span></span> | <span data-ttu-id="090f0-6981">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-6981">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-6982">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-6982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-6983">16</span><span class="sxs-lookup"><span data-stu-id="090f0-6983">16</span></span> |
| <span data-ttu-id="090f0-6984">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-6984">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-6986">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6986">Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6987">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-6987">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6988">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-6988">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6989">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-6989">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-6990">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-6990">Texture1D</span></span> | \- |
| <span data-ttu-id="090f0-6991">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-6991">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-6993">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-6993">Texture3D</span></span> | \- |
| <span data-ttu-id="090f0-6994">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-6994">TextureCube</span></span> | \- |
| <span data-ttu-id="090f0-6995">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-6995">Shader ld</span></span> | \- |
| <span data-ttu-id="090f0-6996">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6996">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="090f0-6997">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6997">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-6998">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-6998">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-6999">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-6999">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-7000">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-7000">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-7001">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-7001">Mipmap</span></span> | \- |
| <span data-ttu-id="090f0-7002">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-7002">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="090f0-7003">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-7003">RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-7004">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-7004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-7005">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-7005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-7006">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-7006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-7007">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-7007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-7008">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-7008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-7009">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-7009">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-7010">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-7010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-7011">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-7011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-7012">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-7012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-7013">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-7013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-7014">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-7014">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-7015">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-7015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-7016">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-7016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-7017">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-7017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-7018">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-7018">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-7020">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-7020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-7021">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-7021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="090f0-7022">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-7022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="090f0-7023">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-7023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="090f0-7024">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-7024">Multisample Load</span></span> | \- |
| <span data-ttu-id="090f0-7025">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-7025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-7026">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-7026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-7027">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-7027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-7028">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-7028">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-7030">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-7030">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-7031">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-7031">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-7032">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-7032">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="090f0-7033">DXGI_FORMAT_B4G4R4A4 \_ unorm<sup></sup> -Fehler (115)</span><span class="sxs-lookup"><span data-stu-id="090f0-7033">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="090f0-7034">Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-7034">Target</span></span> | <span data-ttu-id="090f0-7035">Support</span><span class="sxs-lookup"><span data-stu-id="090f0-7035">Support</span></span> |
| - | - |
| <span data-ttu-id="090f0-7036">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="090f0-7036">Bits Per Element (BPE)</span></span> | <span data-ttu-id="090f0-7037">16</span><span class="sxs-lookup"><span data-stu-id="090f0-7037">16</span></span> |
| <span data-ttu-id="090f0-7038">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="090f0-7038">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-7040">Buffer</span><span class="sxs-lookup"><span data-stu-id="090f0-7040">Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-7042">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="090f0-7042">Input Assembler Vertex Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-7044">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="090f0-7044">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="090f0-7045">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="090f0-7045">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="090f0-7046">Texture1D</span><span class="sxs-lookup"><span data-stu-id="090f0-7046">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-7048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="090f0-7048">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-7050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="090f0-7050">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-7052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="090f0-7052">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-7054">Shader LD</span><span class="sxs-lookup"><span data-stu-id="090f0-7054">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-7056">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-7056">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-7058">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-7058">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="090f0-7059">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="090f0-7059">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="090f0-7060">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="090f0-7060">Shader gather4</span></span> | \- |
| <span data-ttu-id="090f0-7061">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="090f0-7061">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="090f0-7062">MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-7062">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-7064">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="090f0-7064">Mipmap Auto-Generation</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-7066">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-7066">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-7068">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-7068">Blendable RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-7070">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="090f0-7070">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="090f0-7071">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="090f0-7071">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="090f0-7072">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-7072">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-7073">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="090f0-7073">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="090f0-7074">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="090f0-7074">Typed UAV</span></span> | \- |
| <span data-ttu-id="090f0-7075">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="090f0-7075">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="090f0-7076">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-7076">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="090f0-7077">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="090f0-7077">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="090f0-7078">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="090f0-7078">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="090f0-7079">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="090f0-7079">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="090f0-7080">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="090f0-7080">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="090f0-7081">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="090f0-7081">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-7082">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="090f0-7082">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="090f0-7083">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="090f0-7083">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-7085">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-7085">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-7087">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="090f0-7087">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-7089">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="090f0-7089">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-7091">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="090f0-7091">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="090f0-7093">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="090f0-7093">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="090f0-7095">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="090f0-7095">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="090f0-7096">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="090f0-7096">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="090f0-7097">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="090f0-7097">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="090f0-7098">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-7098">Video Processor Input</span></span> | \- |
| <span data-ttu-id="090f0-7099">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="090f0-7099">Video Processor Output</span></span> | \- |
| <span data-ttu-id="090f0-7100">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-7100">Shared Resource</span></span> | \- |
| <span data-ttu-id="090f0-7101">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="090f0-7101">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="090f0-7102">Notizen formatieren</span><span class="sxs-lookup"><span data-stu-id="090f0-7102">Format notes</span></span>

<span data-ttu-id="090f0-7103">Der Zweck des-Formats kann sich von einer Hardware Funktionsebene zur nächsten ändern.</span><span class="sxs-lookup"><span data-stu-id="090f0-7103">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="090f0-7104"><sup>L</sup> : typloses Format</span><span class="sxs-lookup"><span data-stu-id="090f0-7104"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="090f0-7105"><sup>PCs</sup> : teilweise typisiertes, castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="090f0-7105"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="090f0-7106"><sup>FCS</sup> : vollständig typisiertes, castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="090f0-7106"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="090f0-7107"><sup>FNS</sup> : vollständig typisiertes, nicht-castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="090f0-7107"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="090f0-7108"><sup>PCC</sup> : teilweise typisiertes, castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="090f0-7108"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="090f0-7109"><sup>FCC</sup> : vollständig typisiertes, castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="090f0-7109"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="090f0-7110"><sup>FNC</sup> : vollständig typisiertes, nicht-castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="090f0-7110"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="090f0-7111"><sup>V</sup> : Videoformat</span><span class="sxs-lookup"><span data-stu-id="090f0-7111"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="090f0-7112">Backpuffer und Scanvorgänge im [**DXGI- \_ Format \_ R16G16B16A16 \_ float**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Format enthalten lineare Gamma-Daten.</span><span class="sxs-lookup"><span data-stu-id="090f0-7112">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="090f0-7113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="090f0-7113">Related topics</span></span>

[<span data-ttu-id="090f0-7114">D3D12-Hardware Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="090f0-7114">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="090f0-7115">**ID3D10Device:: checkformatsupport**</span><span class="sxs-lookup"><span data-stu-id="090f0-7115">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="090f0-7116">Programmier Handbuch für DXGI</span><span class="sxs-lookup"><span data-stu-id="090f0-7116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
