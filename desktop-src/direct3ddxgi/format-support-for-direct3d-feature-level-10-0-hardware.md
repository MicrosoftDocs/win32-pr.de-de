---
description: In diesem Abschnitt werden die Formate ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die auf Direct3D Feature Level 10,0-Hardware unterstützt werden.
ms.assetid: 3C1CCA7D-9F2F-4B1B-8424-BA9C6DED4974
title: Formatunterstützung für Direct3D 10.0-Hardware auf Featureebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f298460330feb2143b20da37ae82c3a6d63790
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213856"
---
# <a name="format-support-for-direct3d-feature-level-100-hardware"></a><span data-ttu-id="a2762-103">Formatunterstützung für Direct3D 10.0-Hardware auf Featureebene</span><span class="sxs-lookup"><span data-stu-id="a2762-103">Format support for Direct3D Feature Level 10.0 hardware</span></span>

<span data-ttu-id="a2762-104">In diesem Abschnitt werden die Formate ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die auf Direct3D Feature Level 10,0-Hardware unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a2762-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.0 hardware.</span></span>

<span data-ttu-id="a2762-105">Die Tabelle enthält eine Zusammenfassung der Featureunterstützung, die den folgenden Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2762-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="a2762-106">Symbol</span><span class="sxs-lookup"><span data-stu-id="a2762-106">Symbol</span></span>                            | <span data-ttu-id="a2762-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2762-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="a2762-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="a2762-108">_ *-*\*</span></span>                             | <span data-ttu-id="a2762-109">Nicht zulässig oder nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a2762-109">Disallowed or not available.</span></span>                                                  |
| ![Erforderlich](images/letter-r.jpg)  | <span data-ttu-id="a2762-111">Hardware Unterstützung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a2762-111">Hardware support is required.</span></span>                                                 |
| ![Optional](images/letter-o.jpg)  | <span data-ttu-id="a2762-113">Hardwareunterstützung optional, das Format ist möglicherweise Hardware beschleunigt.</span><span class="sxs-lookup"><span data-stu-id="a2762-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![lässe](images/letter-d.jpg) | <span data-ttu-id="a2762-115">Erforderlich, wenn eine zugehörige optionale Funktion unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a2762-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="a2762-116">Dieses Thema enthält einen Abschnitt Pro Format.</span><span class="sxs-lookup"><span data-stu-id="a2762-116">This topic contains a section per format.</span></span> <span data-ttu-id="a2762-117">Ein Format *Ziel* (die Tabellen enthalten eine Zeile pro Ziel) kann ein Ressourcentyp, eine intrinsische HLSL-Funktion oder eine bestimmte Funktionalität sein, die von einem bestimmten Format abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="a2762-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="a2762-118">Informationen zur programmgesteuerten Überprüfung der Formatunterstützung in D3D11 und D3D12 finden Sie unter über [Prüfen der Unterstützung von Hardwarefunktionen](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="a2762-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="a2762-119">Die Zahlen der Formate sind größtenteils, aber nicht alle in aufsteigender numerischer Reihenfolge, dass einige nicht in &mdash; numerischer Reihenfolge sind und neben anderen relevanten Formaten aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a2762-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="a2762-120">Beachten Sie auch, dass *typlose* in einem Format Namen *teilweise* typisiert und nicht streng typlos sein kann (Weitere Informationen finden Sie im Abschnitt " [Format Notizen](#format-notes) " am Ende des Themas).</span><span class="sxs-lookup"><span data-stu-id="a2762-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>
 
## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="a2762-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="a2762-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="a2762-122">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-122">Target</span></span> | <span data-ttu-id="a2762-123">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-123">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-124">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-125">0</span><span class="sxs-lookup"><span data-stu-id="a2762-125">0</span></span> |
| <span data-ttu-id="a2762-126">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-126">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-128">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-130">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-131">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-132">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-133">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-134">Texture2D</span></span> | \- |
| <span data-ttu-id="a2762-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-135">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-136">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-137">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-137">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-138">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-139">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-140">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-141">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-142">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-143">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-143">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-144">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-146">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-147">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-148">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-149">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-150">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-151">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-152">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-153">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-154">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-155">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-157">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-158">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-159">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-160">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-160">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-162">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-163">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-164">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-165">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-166">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-167">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-168">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-169">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-170">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-171">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-172">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-173">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="a2762-174">DXGI_FORMAT_R32G32B32A32 \_ Typen losen<sup>PCs</sup> (1)</span><span class="sxs-lookup"><span data-stu-id="a2762-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="a2762-175">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-175">Target</span></span> | <span data-ttu-id="a2762-176">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-176">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-177">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-178">128</span><span class="sxs-lookup"><span data-stu-id="a2762-178">128</span></span> |
| <span data-ttu-id="a2762-179">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-179">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-181">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-181">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-182">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-183">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-184">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-185">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-187">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-189">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-191">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-193">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-193">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-194">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-195">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-196">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-197">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-198">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-199">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-199">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-201">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-202">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-203">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-204">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-205">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-206">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-207">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-208">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-209">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-210">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-211">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-212">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-213">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-214">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-215">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-216">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-217">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-217">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-219">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-220">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-221">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-222">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-223">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-224">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-225">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-225">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-227">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-228">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-229">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-230">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-230">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-232">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="a2762-233">DXGI_FORMAT_R32G32B32A32 \_ float<sup></sup> -Zeichen (2)</span><span class="sxs-lookup"><span data-stu-id="a2762-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="a2762-234">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-234">Target</span></span> | <span data-ttu-id="a2762-235">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-235">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-236">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-237">128</span><span class="sxs-lookup"><span data-stu-id="a2762-237">128</span></span> |
| <span data-ttu-id="a2762-238">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-238">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-240">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-240">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-242">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-242">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-244">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-245">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-245">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-247">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-249">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-251">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-253">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-255">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-255">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-257">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-257">Shader sample (any filter)</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-259">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-260">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-261">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-262">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-263">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-263">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-265">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-265">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-267">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-269">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-269">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-271">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-272">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-273">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-274">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-275">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-276">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-277">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-278">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-279">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-280">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-281">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-282">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-283">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-284">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-284">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-286">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-286">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-288">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-288">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-290">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-290">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-292">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-292">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-294">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-294">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-296">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-297">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-297">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-299">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-300">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-301">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-302">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-302">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-304">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="a2762-305">DXGI_FORMAT_R32G32B32A32 \_ uint-<sup>f</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="a2762-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="a2762-306">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-306">Target</span></span> | <span data-ttu-id="a2762-307">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-307">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-308">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-309">128</span><span class="sxs-lookup"><span data-stu-id="a2762-309">128</span></span> |
| <span data-ttu-id="a2762-310">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-310">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-312">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-312">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-314">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-314">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-316">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-317">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-317">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-319">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-321">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-323">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-325">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-327">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-327">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-329">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-330">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-331">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-332">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-333">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-334">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-334">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-336">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-337">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-337">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-339">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-340">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-340">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-342">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-343">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-344">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-345">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-346">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-347">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-348">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-349">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-350">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-351">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-352">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-353">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-354">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-354">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-356">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-356">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-358">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-358">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-360">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-360">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-362">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-363">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-363">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-365">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-366">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-366">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-368">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-369">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-370">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-371">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-371">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-373">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="a2762-374">DXGI_FORMAT_R32G32B32A32 \_ Sint<sup></sup> (4)</span><span class="sxs-lookup"><span data-stu-id="a2762-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="a2762-375">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-375">Target</span></span> | <span data-ttu-id="a2762-376">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-376">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-377">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-378">128</span><span class="sxs-lookup"><span data-stu-id="a2762-378">128</span></span> |
| <span data-ttu-id="a2762-379">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-379">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-381">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-381">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-383">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-383">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-385">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-386">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-386">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-388">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-390">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-392">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-394">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-396">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-396">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-398">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-399">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-400">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-401">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-402">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-403">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-403">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-405">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-406">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-408">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-409">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-410">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-411">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-412">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-413">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-414">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-415">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-416">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-417">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-419">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-420">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-421">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-422">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-422">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-424">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-424">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-426">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-426">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-428">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-428">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-430">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-431">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-431">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-433">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-434">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-434">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-436">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-437">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-438">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-439">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-439">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-441">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="a2762-442">DXGI_FORMAT_R32G32B32 \_ Typen losen<sup>PCs</sup> (5)</span><span class="sxs-lookup"><span data-stu-id="a2762-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="a2762-443">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-443">Target</span></span> | <span data-ttu-id="a2762-444">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-444">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-445">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-446">96</span><span class="sxs-lookup"><span data-stu-id="a2762-446">96</span></span> |
| <span data-ttu-id="a2762-447">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-447">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-449">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-449">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-450">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-451">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-452">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-453">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-455">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-457">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-459">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-461">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-461">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-462">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-463">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-464">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-465">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-466">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-467">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-467">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-469">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-471">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-472">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-473">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-474">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-475">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-476">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-477">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-478">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-479">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-480">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-482">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-483">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-484">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-485">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-485">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-487">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-488">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-489">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-490">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-491">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-492">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-493">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-493">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-495">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-496">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-497">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-498">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-499">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="a2762-500">DXGI_FORMAT_R32G32B32 \_ float<sup></sup> -Zeichen (6)</span><span class="sxs-lookup"><span data-stu-id="a2762-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="a2762-501">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-501">Target</span></span> | <span data-ttu-id="a2762-502">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-502">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-503">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-504">96</span><span class="sxs-lookup"><span data-stu-id="a2762-504">96</span></span> |
| <span data-ttu-id="a2762-505">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-505">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-507">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-507">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-509">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-509">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-511">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-512">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-512">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-514">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-516">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-518">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-520">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-522">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-522">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-524">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-524">Shader sample (any filter)</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-526">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-527">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-528">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-529">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-530">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-530">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-532">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-532">Mipmap Auto-Generation</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-534">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-536">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-536">Blendable RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="a2762-538">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-539">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-540">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-541">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-542">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-543">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-544">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-545">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-546">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-547">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-548">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-549">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-550">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-551">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-551">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-553">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-553">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="a2762-555">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-555">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="a2762-557">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-557">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-559">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-559">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-561">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-561">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-563">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-564">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-564">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-566">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-567">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-568">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-569">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-570">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="a2762-571">DXGI_FORMAT_R32G32B32 \_ uint-<sup>f</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="a2762-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="a2762-572">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-572">Target</span></span> | <span data-ttu-id="a2762-573">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-573">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-574">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-575">96</span><span class="sxs-lookup"><span data-stu-id="a2762-575">96</span></span> |
| <span data-ttu-id="a2762-576">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-576">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-578">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-578">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-580">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-580">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-582">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-583">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-583">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-585">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-587">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-589">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-591">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-593">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-593">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-595">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-596">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-597">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-598">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-599">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-600">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-600">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-602">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-603">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-603">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-605">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-606">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-606">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-608">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-609">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-610">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-611">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-612">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-613">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-614">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-615">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-616">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-617">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-618">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-619">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-620">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-620">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-622">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-622">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="a2762-624">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-624">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="a2762-626">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-626">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-628">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-629">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-629">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-631">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-632">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-632">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-634">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-635">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-636">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-637">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-638">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="a2762-639">DXGI_FORMAT_R32G32B32 \_ Sint<sup></sup> -Karten (8)</span><span class="sxs-lookup"><span data-stu-id="a2762-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="a2762-640">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-640">Target</span></span> | <span data-ttu-id="a2762-641">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-641">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-642">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-643">96</span><span class="sxs-lookup"><span data-stu-id="a2762-643">96</span></span> |
| <span data-ttu-id="a2762-644">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-644">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-646">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-646">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-648">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-648">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-650">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-651">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-651">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-653">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-655">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-657">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-659">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-661">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-661">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-663">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-664">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-665">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-666">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-667">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-668">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-668">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-670">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-671">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-671">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-673">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-674">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-675">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-676">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-677">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-678">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-679">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-680">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-681">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-682">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-684">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-685">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-686">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-687">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-687">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-689">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-689">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="a2762-691">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-691">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="a2762-693">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-693">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-695">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-696">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-696">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-698">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-699">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-699">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-701">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-702">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-703">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-704">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-705">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="a2762-706">DXGI_FORMAT_R16G16B16A16 \_ Typen losen<sup>PCs</sup> (9)</span><span class="sxs-lookup"><span data-stu-id="a2762-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="a2762-707">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-707">Target</span></span> | <span data-ttu-id="a2762-708">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-708">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-709">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-710">64</span><span class="sxs-lookup"><span data-stu-id="a2762-710">64</span></span> |
| <span data-ttu-id="a2762-711">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-711">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-713">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-713">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-714">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-715">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-716">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-717">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-719">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-721">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-723">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-725">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-725">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-726">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-727">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-728">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-729">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-730">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-731">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-731">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-733">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-734">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-735">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-736">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-737">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-738">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-739">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-740">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-741">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-742">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-743">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-744">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-745">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-746">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-747">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-748">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-749">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-749">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-751">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-752">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-753">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-754">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-755">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-756">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-757">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-757">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-759">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-760">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-761">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-762">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-762">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-764">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="a2762-765">DXGI_FORMAT_R16G16B16A16 \_ float<sup></sup> -Zeichen (10)</span><span class="sxs-lookup"><span data-stu-id="a2762-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="a2762-766">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-766">Target</span></span> | <span data-ttu-id="a2762-767">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-767">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-768">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-769">64</span><span class="sxs-lookup"><span data-stu-id="a2762-769">64</span></span> |
| <span data-ttu-id="a2762-770">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-770">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-772">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-772">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-774">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-774">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-776">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-777">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-778">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-780">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-782">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-784">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-786">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-786">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-788">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-788">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-790">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-791">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-792">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-793">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-794">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-794">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-796">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-796">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-798">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-798">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-800">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-800">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-802">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-803">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-804">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-805">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-806">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-807">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-808">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-809">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-810">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-811">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-812">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-813">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-814">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-815">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-815">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-817">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-817">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-819">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-819">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-821">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-821">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-823">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-823">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-825">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-825">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-827">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-827">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-829">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-829">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-831">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-832">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-832">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-834">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-834">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-836">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-836">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-838">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="a2762-839">DXGI_FORMAT_R16G16B16A16 \_ unorm-Datei-<sup>e</sup> /a (11)</span><span class="sxs-lookup"><span data-stu-id="a2762-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="a2762-840">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-840">Target</span></span> | <span data-ttu-id="a2762-841">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-841">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-842">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-843">64</span><span class="sxs-lookup"><span data-stu-id="a2762-843">64</span></span> |
| <span data-ttu-id="a2762-844">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-844">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-846">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-846">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-848">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-848">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-850">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-851">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-852">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-854">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-856">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-858">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-860">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-860">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-862">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-862">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-864">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-865">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-866">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-867">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-868">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-868">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-870">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-870">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-872">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-872">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-874">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-874">Blendable RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-876">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-877">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-878">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-879">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-880">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-881">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-882">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-883">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-884">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-886">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-887">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-888">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-889">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-889">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-891">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-891">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-893">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-893">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-895">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-895">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-897">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-897">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-899">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-899">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-901">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-902">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-902">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-904">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-905">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-906">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-907">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-907">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-909">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="a2762-910">DXGI_FORMAT_R16G16B16A16 \_ uint-<sup>f</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="a2762-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="a2762-911">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-911">Target</span></span> | <span data-ttu-id="a2762-912">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-912">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-913">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-914">64</span><span class="sxs-lookup"><span data-stu-id="a2762-914">64</span></span> |
| <span data-ttu-id="a2762-915">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-915">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-917">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-917">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-919">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-919">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-921">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-922">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-923">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-925">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-927">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-929">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-931">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-931">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-933">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-934">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-935">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-936">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-937">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-938">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-938">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-940">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-941">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-941">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-943">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-944">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-944">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-946">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-947">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-948">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-949">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-950">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-951">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-952">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-953">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-954">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-955">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-956">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-957">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-958">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-958">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-960">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-960">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-962">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-962">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-964">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-964">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-966">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-967">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-967">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-969">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-970">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-970">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-972">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-973">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-974">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-975">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-975">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-977">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="a2762-978">DXGI_FORMAT_R16G16B16A16 \_ snorm<sup></sup> -snorm (13)</span><span class="sxs-lookup"><span data-stu-id="a2762-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="a2762-979">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-979">Target</span></span> | <span data-ttu-id="a2762-980">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-980">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-981">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-982">64</span><span class="sxs-lookup"><span data-stu-id="a2762-982">64</span></span> |
| <span data-ttu-id="a2762-983">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-983">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-985">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-985">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-987">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-987">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-989">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-990">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-991">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-993">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-995">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-997">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-999">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-999">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1001">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1001">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1003">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1004">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1005">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1006">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1007">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1007">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1009">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1009">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1011">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1013">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1013">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1014">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1014">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1015">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1015">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1016">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1016">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1017">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1017">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1018">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1018">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1019">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1019">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1020">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1020">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1021">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1021">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1022">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1022">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1023">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1023">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1024">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1024">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1025">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1025">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1026">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1026">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1027">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1027">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1029">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1029">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1031">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1031">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1033">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1033">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1035">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1035">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1037">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1037">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1039">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1039">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1040">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1040">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1042">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1042">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1043">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1043">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1044">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1044">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1045">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1045">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1047">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1047">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="a2762-1048">DXGI_FORMAT_R16G16B16A16 \_ Sint<sup></sup> (14)</span><span class="sxs-lookup"><span data-stu-id="a2762-1048">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="a2762-1049">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1049">Target</span></span> | <span data-ttu-id="a2762-1050">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1050">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1051">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1051">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1052">64</span><span class="sxs-lookup"><span data-stu-id="a2762-1052">64</span></span> |
| <span data-ttu-id="a2762-1053">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1053">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1055">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1055">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1057">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1057">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1059">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1059">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1060">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1060">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1061">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1061">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1063">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1063">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1065">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1065">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1067">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1067">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1069">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1069">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1071">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1071">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-1072">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1072">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1073">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1073">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1074">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1074">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1075">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1075">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1076">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1076">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1078">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1078">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-1079">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1079">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1081">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1081">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1082">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1082">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1083">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1083">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1084">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1084">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1085">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1085">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1086">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1086">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1087">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1087">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1088">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1088">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1089">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1089">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1090">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1090">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1091">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1091">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1092">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1092">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1093">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1093">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1094">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1094">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1095">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1095">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1097">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1097">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1099">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1099">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1101">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1101">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1103">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1103">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-1104">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1104">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1106">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1106">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1107">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1107">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1109">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1109">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1110">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1110">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1111">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1111">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1112">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1112">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1114">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="a2762-1115">DXGI_FORMAT_R32G32 \_ Typen losen<sup>PCs</sup> (15)</span><span class="sxs-lookup"><span data-stu-id="a2762-1115">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="a2762-1116">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1116">Target</span></span> | <span data-ttu-id="a2762-1117">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1117">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1118">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1119">64</span><span class="sxs-lookup"><span data-stu-id="a2762-1119">64</span></span> |
| <span data-ttu-id="a2762-1120">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1120">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1122">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1122">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1123">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1124">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1125">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1126">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1128">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1130">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1132">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1134">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1134">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-1135">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1135">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-1136">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1136">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1137">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1137">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1138">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1138">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1139">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1139">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1140">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1140">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1142">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-1143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1143">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1144">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1145">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1146">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1147">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1148">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1149">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1149">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1150">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1151">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1152">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1153">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1154">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1155">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1156">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1157">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1158">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1158">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1160">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1160">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1161">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1161">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1162">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1162">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-1163">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1163">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-1164">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1164">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-1165">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1165">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1166">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1166">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1168">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1168">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1169">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1169">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1170">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1170">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1171">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1171">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-1172">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1172">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="a2762-1173">DXGI_FORMAT_R32G32 \_ float<sup></sup> -Zeichen (16)</span><span class="sxs-lookup"><span data-stu-id="a2762-1173">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="a2762-1174">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1174">Target</span></span> | <span data-ttu-id="a2762-1175">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1175">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1176">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1176">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1177">64</span><span class="sxs-lookup"><span data-stu-id="a2762-1177">64</span></span> |
| <span data-ttu-id="a2762-1178">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1178">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1180">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1180">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1182">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1182">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1184">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1185">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1185">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1187">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1189">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1189">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1191">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1191">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1193">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1193">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1195">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1195">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1197">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1197">Shader sample (any filter)</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1199">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1199">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1200">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1200">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1201">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1201">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1202">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1202">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1203">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1203">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1205">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1205">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1207">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1207">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1209">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1209">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1211">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1211">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1212">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1212">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1213">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1213">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1214">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1214">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1215">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1215">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1216">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1216">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1217">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1217">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1218">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1218">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1219">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1219">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1220">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1220">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1221">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1221">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1222">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1222">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1223">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1223">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1224">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1224">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1226">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1226">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1228">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1228">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1230">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1230">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1232">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1232">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1234">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1234">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1236">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1236">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1237">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1237">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1239">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1239">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1240">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1240">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1241">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1241">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1242">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1242">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-1243">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1243">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="a2762-1244">DXGI_FORMAT_R32G32 \_ uint<sup></sup> -Zeichen (17)</span><span class="sxs-lookup"><span data-stu-id="a2762-1244">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="a2762-1245">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1245">Target</span></span> | <span data-ttu-id="a2762-1246">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1246">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1247">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1247">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1248">64</span><span class="sxs-lookup"><span data-stu-id="a2762-1248">64</span></span> |
| <span data-ttu-id="a2762-1249">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1249">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1251">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1251">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1253">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1253">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1255">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1255">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1256">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1256">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1258">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1258">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1260">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1260">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1262">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1262">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1264">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1264">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1266">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1266">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1268">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1268">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-1269">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1269">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1270">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1270">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1271">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1271">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1272">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1272">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1273">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1273">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1275">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1275">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-1276">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1276">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1278">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1278">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1279">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1279">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1281">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1281">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1282">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1282">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1283">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1283">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1284">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1284">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1285">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1285">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1286">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1286">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1287">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1287">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1288">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1288">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1289">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1289">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1290">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1290">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1291">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1291">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1292">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1292">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1293">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1293">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1295">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1295">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1297">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1297">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1299">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1299">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1301">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-1302">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1302">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1304">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1304">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1305">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1305">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1307">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1307">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1308">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1308">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1309">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1309">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1310">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1310">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-1311">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="a2762-1312">DXGI_FORMAT_R32G32 \_ Sint<sup></sup> -Datei (18)</span><span class="sxs-lookup"><span data-stu-id="a2762-1312">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="a2762-1313">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1313">Target</span></span> | <span data-ttu-id="a2762-1314">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1314">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1315">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1316">64</span><span class="sxs-lookup"><span data-stu-id="a2762-1316">64</span></span> |
| <span data-ttu-id="a2762-1317">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1317">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1319">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1319">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1321">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1321">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1323">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1323">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1324">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1324">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1326">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1326">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1328">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1330">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1332">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1332">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1334">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1334">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1336">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1336">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-1337">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1337">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1338">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1338">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1339">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1339">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1340">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1340">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1341">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1341">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1343">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1343">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-1344">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1344">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1346">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1347">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1348">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1349">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1350">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1351">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1351">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1352">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1353">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1354">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1355">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1356">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1356">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1357">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1358">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1359">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1360">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1360">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1362">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1362">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1364">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1364">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1366">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1366">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1368">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-1369">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1369">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1371">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1372">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1372">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1374">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1375">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1376">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1377">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1377">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-1378">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="a2762-1379">DXGI_FORMAT_R32G8X24 \_ Typen losen<sup>PCs</sup> (19)</span><span class="sxs-lookup"><span data-stu-id="a2762-1379">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="a2762-1380">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1380">Target</span></span> | <span data-ttu-id="a2762-1381">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1381">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1382">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1383">64</span><span class="sxs-lookup"><span data-stu-id="a2762-1383">64</span></span> |
| <span data-ttu-id="a2762-1384">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1384">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1386">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1386">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1387">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1387">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1388">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1388">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1389">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1389">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1390">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1390">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1392">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1394">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-1395">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1395">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1397">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1397">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-1398">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-1399">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1400">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1401">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1401">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1402">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1403">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1403">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1405">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-1406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1406">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1407">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1407">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1408">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1408">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1409">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1409">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1410">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1410">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1411">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1411">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1412">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1412">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1413">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1413">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1414">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1414">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1415">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1415">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1416">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1416">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1417">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1417">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1418">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1418">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1419">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1419">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1420">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1420">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1421">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1421">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1423">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1424">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1425">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-1426">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-1427">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1427">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-1428">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1429">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1429">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1431">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1431">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1432">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1432">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1433">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1433">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1434">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1434">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-1435">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1435">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="a2762-1436">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint-<sup>f</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="a2762-1436">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="a2762-1437">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1437">Target</span></span> | <span data-ttu-id="a2762-1438">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1438">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1439">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1439">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1440">64</span><span class="sxs-lookup"><span data-stu-id="a2762-1440">64</span></span> |
| <span data-ttu-id="a2762-1441">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1441">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1443">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1443">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1444">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1445">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1446">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1447">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1449">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1449">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1451">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1451">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-1452">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1452">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1454">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1454">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-1455">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-1456">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1457">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1458">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1459">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1460">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1460">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1462">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1462">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-1463">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1463">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1464">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1464">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1465">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1465">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1466">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1466">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1468">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1469">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1470">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1471">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1472">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1473">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1474">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1475">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1475">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1476">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1477">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1478">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1479">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1479">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1481">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1481">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1483">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1483">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1485">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1485">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1487">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1487">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-1488">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1488">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-1489">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1489">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1490">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1490">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1492">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1492">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1493">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1493">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1494">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1494">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1495">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1495">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-1496">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1496">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="a2762-1497">DXGI_FORMAT_R32 \_ float \_ X8X24 \_ typlose<sup></sup> Rechtschreibfehler (21)</span><span class="sxs-lookup"><span data-stu-id="a2762-1497">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="a2762-1498">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1498">Target</span></span> | <span data-ttu-id="a2762-1499">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1499">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1500">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1500">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1501">64</span><span class="sxs-lookup"><span data-stu-id="a2762-1501">64</span></span> |
| <span data-ttu-id="a2762-1502">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1502">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1504">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1504">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1505">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1505">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1506">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1506">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1507">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1507">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1508">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1508">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1510">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1512">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-1513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1513">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1515">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1515">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1517">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1517">Shader sample (any filter)</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1519">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1519">Shader sample\_c (comparison filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1521">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1521">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1522">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1522">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1523">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1523">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1524">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1524">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1526">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1526">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-1527">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1527">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1528">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1528">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1529">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1529">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1530">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1530">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1531">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1531">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1532">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1532">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1533">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1533">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1534">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1534">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1535">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1535">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1536">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1536">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1537">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1537">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1538">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1538">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1539">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1539">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1540">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1540">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1541">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1541">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1542">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1542">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1544">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1544">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1545">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1545">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1546">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1546">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-1547">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1547">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-1548">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1548">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-1549">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1549">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1550">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1550">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1552">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1552">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1553">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1553">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1554">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1554">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1555">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1555">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-1556">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1556">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="a2762-1557">DXGI_FORMAT_X32 \_ typlose \_ G8X24 \_ uint-<sup>f</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="a2762-1557">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="a2762-1558">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1558">Target</span></span> | <span data-ttu-id="a2762-1559">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1559">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1560">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1560">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1561">64</span><span class="sxs-lookup"><span data-stu-id="a2762-1561">64</span></span> |
| <span data-ttu-id="a2762-1562">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1562">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1564">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1564">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1565">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1565">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1566">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1566">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1567">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1567">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1568">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1568">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1570">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1570">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1572">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1572">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-1573">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1573">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1575">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1575">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1577">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1577">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-1578">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1578">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1579">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1579">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1580">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1580">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1581">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1581">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1582">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1582">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1584">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1584">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-1585">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1585">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1586">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1586">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1587">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1587">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1588">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1588">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1589">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1589">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1590">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1590">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1591">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1591">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1592">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1592">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1593">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1593">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1594">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1594">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1595">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1595">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1596">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1596">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1597">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1597">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1598">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1598">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1599">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1599">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1600">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1600">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1602">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1602">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1603">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1603">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1604">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1604">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-1605">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1605">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-1606">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1606">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-1607">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1607">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1608">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1608">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1610">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1610">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1611">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1611">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1612">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1612">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1613">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1613">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-1614">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1614">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="a2762-1615">DXGI_FORMAT_R10G10B10A2 \_ typlosen<sup>PCs</sup> (23)</span><span class="sxs-lookup"><span data-stu-id="a2762-1615">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="a2762-1616">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1616">Target</span></span> | <span data-ttu-id="a2762-1617">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1617">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1618">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1618">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1619">32</span><span class="sxs-lookup"><span data-stu-id="a2762-1619">32</span></span> |
| <span data-ttu-id="a2762-1620">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1620">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1622">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1622">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1623">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1623">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1624">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1624">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1625">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1625">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1626">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1626">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1628">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1628">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1630">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1630">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1632">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1632">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1634">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1634">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-1635">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1635">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-1636">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1636">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1637">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1637">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1638">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1638">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1639">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1639">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1640">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1640">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1642">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1642">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-1643">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1643">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1644">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1644">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1645">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1645">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1646">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1646">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1647">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1647">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1648">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1648">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1649">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1649">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1650">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1650">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1651">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1651">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1652">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1652">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1653">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1653">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1654">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1654">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1655">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1655">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1656">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1656">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1657">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1657">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1658">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1658">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1660">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1660">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1661">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1661">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1662">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1662">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-1663">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1663">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-1664">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1664">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-1665">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1665">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1666">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1666">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1668">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1669">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1670">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1671">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1671">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1673">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1673">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="a2762-1674">DXGI_FORMAT_R10G10B10A2 \_ unorm-Datei-<sup>e</sup> /a (24)</span><span class="sxs-lookup"><span data-stu-id="a2762-1674">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="a2762-1675">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1675">Target</span></span> | <span data-ttu-id="a2762-1676">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1676">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1677">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1677">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1678">32</span><span class="sxs-lookup"><span data-stu-id="a2762-1678">32</span></span> |
| <span data-ttu-id="a2762-1679">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1679">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1681">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1681">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1683">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1683">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1685">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1685">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1686">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1686">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1687">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1687">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1689">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1689">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1691">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1691">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1693">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1693">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1695">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1695">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1697">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1697">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1699">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1700">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1701">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1701">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1702">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1703">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1703">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1705">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1705">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1707">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1707">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1709">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1709">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1711">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1711">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1712">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1712">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1713">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1713">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1714">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1714">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1715">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1715">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1716">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1716">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1717">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1717">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1718">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1718">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1719">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1719">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1720">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1720">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1721">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1721">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1722">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1722">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1723">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1723">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1724">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1724">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1726">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1726">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1728">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1728">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1730">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1730">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1732">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1732">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1734">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1734">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1736">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1736">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1738">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1738">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1740">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1741">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1741">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1743">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1743">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1745">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1745">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1747">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1747">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="a2762-1748">DXGI_FORMAT_R10G10B10A2 \_ uint<sup></sup> -Zeichen (25)</span><span class="sxs-lookup"><span data-stu-id="a2762-1748">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="a2762-1749">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1749">Target</span></span> | <span data-ttu-id="a2762-1750">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1750">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1751">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1751">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1752">32</span><span class="sxs-lookup"><span data-stu-id="a2762-1752">32</span></span> |
| <span data-ttu-id="a2762-1753">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1753">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1755">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1755">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1757">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1757">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1759">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1760">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1761">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1763">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1765">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1765">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1767">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1767">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1769">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1769">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1771">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1771">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-1772">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1772">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1773">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1773">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1774">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1774">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1775">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1775">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1776">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1776">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1778">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1778">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-1779">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1779">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1781">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1781">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1782">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1782">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1784">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1785">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1786">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1787">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1787">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1788">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1789">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1790">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1791">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1792">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1793">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1794">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1795">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1796">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1796">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1798">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1798">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1800">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1800">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1802">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1802">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1804">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-1805">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1805">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1807">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1807">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1808">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1808">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1810">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1810">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1811">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1811">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1812">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1812">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1813">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1813">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1815">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1815">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="a2762-1816">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ unorm-Datei-<sup>e</sup> /a (89)</span><span class="sxs-lookup"><span data-stu-id="a2762-1816">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="a2762-1817">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1817">Target</span></span> | <span data-ttu-id="a2762-1818">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1818">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1819">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1819">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1820">32</span><span class="sxs-lookup"><span data-stu-id="a2762-1820">32</span></span> |
| <span data-ttu-id="a2762-1821">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1821">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1823">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1823">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1824">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1824">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1825">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1825">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1826">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1826">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1827">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1827">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-1828">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1828">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1830">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1830">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-1831">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1831">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-1832">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1832">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-1833">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1833">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-1834">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1834">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1835">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1835">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1836">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1836">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1837">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1837">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1838">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1838">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-1839">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1839">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-1840">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1840">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1841">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1841">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1842">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1842">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1843">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1843">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1844">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1845">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1846">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1846">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1847">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1848">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1849">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1850">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1851">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1852">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1853">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1854">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1855">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1855">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1857">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1857">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1858">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1858">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1859">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1859">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-1860">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1860">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-1861">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1861">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-1862">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1862">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1864">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1864">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1866">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1866">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1867">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1867">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1869">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1869">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1871">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1871">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1873">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="a2762-1874">DXGI_FORMAT_R11G11B10 \_ float<sup></sup> -Datentyp (26)</span><span class="sxs-lookup"><span data-stu-id="a2762-1874">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="a2762-1875">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1875">Target</span></span> | <span data-ttu-id="a2762-1876">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1876">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1877">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1878">32</span><span class="sxs-lookup"><span data-stu-id="a2762-1878">32</span></span> |
| <span data-ttu-id="a2762-1879">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1879">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1881">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1881">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1883">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1883">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1885">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1886">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1886">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1887">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1887">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1889">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1889">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1891">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1893">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1893">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1895">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1895">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1897">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1897">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1899">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1899">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1900">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1900">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1901">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1901">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1902">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1902">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1903">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1903">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1905">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1905">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1907">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1909">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1909">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1911">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1912">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1913">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1914">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1915">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1915">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1916">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1917">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1918">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1919">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1920">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1920">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1921">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1922">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1923">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1924">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1924">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1926">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1926">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1928">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1928">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1930">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1930">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1932">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1932">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1934">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1934">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-1936">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1936">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1937">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1937">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-1938">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1938">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1939">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1939">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1940">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1940">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1941">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1941">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-1942">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1942">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="a2762-1943">DXGI_FORMAT_R8G8B8A8 \_ typlosen<sup>PCs</sup> (27)</span><span class="sxs-lookup"><span data-stu-id="a2762-1943">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="a2762-1944">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1944">Target</span></span> | <span data-ttu-id="a2762-1945">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-1945">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-1946">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-1946">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-1947">32</span><span class="sxs-lookup"><span data-stu-id="a2762-1947">32</span></span> |
| <span data-ttu-id="a2762-1948">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-1948">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1950">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1950">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1951">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-1951">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1952">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-1952">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1953">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-1953">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-1954">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-1954">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1956">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-1956">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1958">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-1958">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1960">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-1960">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1962">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-1962">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-1963">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1963">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-1964">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1964">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-1965">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-1965">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-1966">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-1966">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-1967">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-1967">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-1968">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1968">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1970">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-1970">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-1971">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1971">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1972">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1972">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1973">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-1973">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-1974">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-1974">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-1975">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1975">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1976">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-1976">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-1977">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-1977">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-1978">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-1978">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-1979">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1979">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-1980">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-1980">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-1981">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-1981">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-1982">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-1982">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-1983">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-1983">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-1984">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-1984">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1985">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-1985">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-1986">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-1986">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1988">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1988">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1989">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-1989">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-1990">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-1990">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-1991">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-1991">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-1992">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-1992">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-1993">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-1993">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-1994">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-1994">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-1996">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-1996">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-1997">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1997">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-1998">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-1998">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-1999">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-1999">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2001">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2001">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="a2762-2002">DXGI_FORMAT_R8G8B8A8 \_ unorm-Datei-<sup>e</sup> /a (28)</span><span class="sxs-lookup"><span data-stu-id="a2762-2002">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="a2762-2003">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2003">Target</span></span> | <span data-ttu-id="a2762-2004">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2004">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2005">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2005">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2006">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2006">32</span></span> |
| <span data-ttu-id="a2762-2007">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2007">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2009">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2009">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2011">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2011">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2013">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2013">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2014">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2014">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2015">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2015">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2017">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2017">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2019">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2019">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2021">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2021">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2023">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2023">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2025">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2025">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2027">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2027">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2028">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2028">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2029">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2029">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2030">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2030">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2031">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2031">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2033">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2033">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2035">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2035">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2037">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2037">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2039">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-2040">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2041">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2042">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2043">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2043">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2044">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2045">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2046">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2047">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2048">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2048">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2049">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2050">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2051">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2052">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2052">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2054">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2054">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2056">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2056">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2058">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2058">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2060">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2060">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2062">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2062">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2064">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2064">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2066">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2066">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2068">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2068">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2069">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2069">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2071">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2071">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2073">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2073">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2075">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="a2762-2076">DXGI_FORMAT_R8G8B8A8 \_ unorm \_ sRGB-<sup>FICS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="a2762-2076">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="a2762-2077">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2077">Target</span></span> | <span data-ttu-id="a2762-2078">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2078">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2079">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2080">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2080">32</span></span> |
| <span data-ttu-id="a2762-2081">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2081">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2083">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2083">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2084">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2085">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2086">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2087">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2089">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2091">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2093">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2095">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2095">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2097">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2097">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2099">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2100">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2101">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2101">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2102">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2103">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2103">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2105">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2105">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2107">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2107">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2109">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2109">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2111">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-2112">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2113">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2114">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2115">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2115">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2116">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2117">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2118">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2119">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2120">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2120">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2121">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2122">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2123">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2124">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2124">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2126">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2126">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2128">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2128">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2130">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2130">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2132">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2132">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2134">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2134">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2136">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2136">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2138">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2138">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2140">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2140">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2141">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2141">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2143">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2143">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2145">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2145">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2147">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="a2762-2148">DXGI_FORMAT_R8G8B8A8 \_ uint<sup></sup> -Zeichen (30)</span><span class="sxs-lookup"><span data-stu-id="a2762-2148">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="a2762-2149">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2149">Target</span></span> | <span data-ttu-id="a2762-2150">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2150">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2151">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2152">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2152">32</span></span> |
| <span data-ttu-id="a2762-2153">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2153">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2155">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2155">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2157">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2157">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2159">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2159">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2160">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2160">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2161">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2161">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2163">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2163">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2165">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2165">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2167">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2167">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2169">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2169">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2171">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2171">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-2172">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2172">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2173">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2173">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2174">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2174">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2175">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2175">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2176">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2176">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2178">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2178">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-2179">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2179">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2181">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2181">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2182">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2182">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2184">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2184">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2185">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2185">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2186">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2186">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2187">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2187">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2188">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2188">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2189">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2189">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2190">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2190">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2191">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2191">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2192">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2192">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2193">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2193">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2194">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2194">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2195">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2195">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2196">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2196">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2198">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2198">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2200">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2200">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2202">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2202">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2204">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2204">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-2205">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2205">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2207">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2207">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-2208">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2208">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2210">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2210">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2211">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2211">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-2212">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2212">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-2213">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2213">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2215">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2215">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="a2762-2216">DXGI_FORMAT_R8G8B8A8 \_ snorm<sup></sup> -snorm (31)</span><span class="sxs-lookup"><span data-stu-id="a2762-2216">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="a2762-2217">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2217">Target</span></span> | <span data-ttu-id="a2762-2218">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2218">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2219">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2219">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2220">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2220">32</span></span> |
| <span data-ttu-id="a2762-2221">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2221">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2223">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2223">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2225">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2225">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2227">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2227">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2228">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2228">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2229">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2229">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2231">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2231">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2233">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2233">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2235">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2235">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2237">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2237">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2239">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2239">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2241">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2241">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2242">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2242">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2243">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2243">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2244">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2244">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2245">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2245">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2247">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2247">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2249">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2249">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2251">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2251">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2252">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2252">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-2253">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2253">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2254">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2254">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2255">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2255">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2256">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2256">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2257">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2257">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2258">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2258">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2259">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2259">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2260">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2260">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2261">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2261">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2262">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2262">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2263">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2263">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2264">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2264">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2265">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2265">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2267">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2267">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2269">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2269">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2271">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2271">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2273">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2273">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2275">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2275">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2277">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2277">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-2278">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2278">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2280">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2281">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-2282">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-2283">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2283">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2285">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2285">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="a2762-2286">DXGI_FORMAT_R8G8B8A8 \_ Sint<sup></sup> -Werte (32)</span><span class="sxs-lookup"><span data-stu-id="a2762-2286">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="a2762-2287">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2287">Target</span></span> | <span data-ttu-id="a2762-2288">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2288">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2289">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2289">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2290">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2290">32</span></span> |
| <span data-ttu-id="a2762-2291">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2291">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2293">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2293">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2295">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2295">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2297">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2298">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2299">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2301">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2301">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2303">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2305">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2305">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2307">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2307">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2309">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2309">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-2310">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2310">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2311">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2311">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2312">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2312">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2313">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2313">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2314">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2314">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2316">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2316">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-2317">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2317">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2319">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2319">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2320">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2320">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-2321">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2321">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2322">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2322">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2323">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2323">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2324">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2324">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2325">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2325">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2326">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2326">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2327">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2327">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2328">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2328">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2329">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2329">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2330">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2330">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2331">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2331">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2332">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2332">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2333">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2333">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2335">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2335">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2337">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2337">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2339">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2339">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2341">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2341">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-2342">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2342">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2344">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-2345">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2345">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2347">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2348">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-2349">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-2350">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2350">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2352">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2352">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="a2762-2353">DXGI_FORMAT_R16G16 \_ Typen losen<sup>PCs</sup> (33)</span><span class="sxs-lookup"><span data-stu-id="a2762-2353">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="a2762-2354">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2354">Target</span></span> | <span data-ttu-id="a2762-2355">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2355">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2356">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2356">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2357">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2357">32</span></span> |
| <span data-ttu-id="a2762-2358">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2358">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2360">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2360">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2361">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2361">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2362">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2362">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2363">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2363">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2364">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2364">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2366">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2366">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2368">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2368">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2370">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2370">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2372">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2372">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-2373">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2373">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-2374">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2375">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2376">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2376">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2377">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2378">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2378">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2380">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-2381">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2381">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2382">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2383">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-2384">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2385">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2386">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2387">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2387">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2388">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2389">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2390">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2391">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2392">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2393">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2394">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2395">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2396">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2396">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2398">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2399">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2400">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-2401">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-2402">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2402">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-2403">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-2404">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2404">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2406">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2407">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-2408">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-2409">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2409">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-2410">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="a2762-2411">DXGI_FORMAT_R16G16 \_ float<sup></sup> -Zeichen (34)</span><span class="sxs-lookup"><span data-stu-id="a2762-2411">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="a2762-2412">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2412">Target</span></span> | <span data-ttu-id="a2762-2413">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2413">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2414">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2415">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2415">32</span></span> |
| <span data-ttu-id="a2762-2416">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2416">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2418">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2418">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2420">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2420">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2422">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2422">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2423">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2423">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2424">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2424">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2426">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2426">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2428">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2428">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2430">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2430">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2432">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2432">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2434">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2434">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2436">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2436">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2437">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2437">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2438">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2438">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2439">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2439">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2440">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2440">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2442">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2442">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2444">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2444">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2446">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2446">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2448">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2448">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-2449">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2449">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2450">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2450">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2451">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2451">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2452">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2452">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2453">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2453">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2454">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2454">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2455">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2455">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2456">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2456">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2457">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2457">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2458">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2458">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2459">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2459">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2460">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2460">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2461">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2461">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2463">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2463">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2465">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2465">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2467">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2467">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2469">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2469">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2471">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2471">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2473">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-2474">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2474">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2476">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2476">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2477">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2477">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-2478">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2478">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-2479">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2479">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-2480">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2480">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="a2762-2481">DXGI_FORMAT_R16G16 \_ unorm-Datei-<sup>e</sup> /a (35)</span><span class="sxs-lookup"><span data-stu-id="a2762-2481">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="a2762-2482">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2482">Target</span></span> | <span data-ttu-id="a2762-2483">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2483">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2484">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2484">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2485">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2485">32</span></span> |
| <span data-ttu-id="a2762-2486">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2486">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2488">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2488">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2490">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2490">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2492">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2493">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2494">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2496">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2496">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2498">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2498">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2500">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2502">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2502">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2504">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2504">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2506">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2507">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2508">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2508">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2509">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2510">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2510">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2512">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2512">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2514">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2516">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2516">Blendable RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2518">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2518">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-2519">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2519">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2520">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2520">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2521">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2521">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2522">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2522">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2523">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2523">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2524">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2524">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2525">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2525">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2526">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2526">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2527">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2527">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2528">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2528">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2529">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2529">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2530">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2530">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2531">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2531">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2533">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2533">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2535">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2535">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2537">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2537">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2539">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2539">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2541">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2541">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2543">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-2544">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2544">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2546">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2546">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2547">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2547">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-2548">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2548">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-2549">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2549">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-2550">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="a2762-2551">DXGI_FORMAT_R16G16 \_ uint-<sup>f</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="a2762-2551">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="a2762-2552">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2552">Target</span></span> | <span data-ttu-id="a2762-2553">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2553">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2554">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2555">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2555">32</span></span> |
| <span data-ttu-id="a2762-2556">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2556">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2558">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2558">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2560">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2560">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2562">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2563">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2564">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2566">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2566">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2568">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2568">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2570">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2570">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2572">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2572">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2574">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2574">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-2575">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2575">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2576">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2576">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2577">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2577">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2578">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2578">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2579">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2579">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2581">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2581">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-2582">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2582">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2584">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2584">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2585">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2585">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2587">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2587">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2588">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2588">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2589">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2589">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2590">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2590">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2591">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2591">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2592">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2592">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2593">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2593">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2594">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2594">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2595">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2595">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2596">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2596">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2597">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2597">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2598">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2598">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2599">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2599">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2601">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2601">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2603">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2603">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2605">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2605">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2607">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2607">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-2608">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2608">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2610">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2610">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-2611">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2611">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2613">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2613">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2614">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2614">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-2615">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2615">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-2616">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2616">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-2617">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2617">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="a2762-2618">DXGI_FORMAT_R16G16 \_ snorm<sup></sup> -snorm (37)</span><span class="sxs-lookup"><span data-stu-id="a2762-2618">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="a2762-2619">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2619">Target</span></span> | <span data-ttu-id="a2762-2620">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2620">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2621">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2621">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2622">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2622">32</span></span> |
| <span data-ttu-id="a2762-2623">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2623">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2625">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2625">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2627">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2627">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2629">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2629">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2630">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2630">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2631">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2631">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2633">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2633">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2635">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2635">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2637">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2637">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2639">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2639">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2641">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2641">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2643">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2643">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2644">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2644">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2645">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2645">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2646">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2646">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2647">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2647">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2649">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2649">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2651">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2651">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2653">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2653">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2654">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2654">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-2655">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2655">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2656">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2656">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2657">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2657">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2658">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2658">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2659">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2659">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2660">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2660">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2661">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2661">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2662">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2662">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2663">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2663">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2664">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2664">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2665">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2665">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2666">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2666">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2667">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2667">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2669">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2669">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2671">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2671">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2673">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2673">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2675">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2675">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2677">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2677">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2679">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2679">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-2680">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2680">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2682">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2682">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2683">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2683">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-2684">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2684">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-2685">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2685">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-2686">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2686">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="a2762-2687">DXGI_FORMAT_R16G16 \_ Sint<sup></sup> -Werte (38)</span><span class="sxs-lookup"><span data-stu-id="a2762-2687">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="a2762-2688">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2688">Target</span></span> | <span data-ttu-id="a2762-2689">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2689">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2690">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2690">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2691">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2691">32</span></span> |
| <span data-ttu-id="a2762-2692">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2692">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2694">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2694">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2696">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2696">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2698">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2698">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2699">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2699">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2700">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2700">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2702">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2702">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2704">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2704">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2706">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2706">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2708">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2708">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2710">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-2711">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2712">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2713">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2713">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2714">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2715">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2715">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2717">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2717">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-2718">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2718">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2720">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2720">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2721">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2721">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-2722">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2722">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2723">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2723">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2724">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2724">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2725">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2725">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2726">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2726">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2727">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2727">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2728">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2728">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2729">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2729">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2730">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2730">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2731">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2731">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2732">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2732">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2733">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2733">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2734">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2734">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2736">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2736">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2738">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2738">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2740">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2740">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2742">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-2743">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2743">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2745">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-2746">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2746">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2748">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2748">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2749">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2749">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-2750">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2750">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-2751">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2751">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-2752">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2752">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="a2762-2753">DXGI_FORMAT_R32 \_ Typen losen<sup>PCs</sup> (39)</span><span class="sxs-lookup"><span data-stu-id="a2762-2753">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="a2762-2754">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2754">Target</span></span> | <span data-ttu-id="a2762-2755">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2755">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2756">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2756">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2757">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2757">32</span></span> |
| <span data-ttu-id="a2762-2758">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2758">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2760">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2760">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2761">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2761">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2762">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2762">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2763">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2763">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2764">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2764">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2766">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2766">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2768">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2768">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2770">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2772">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2772">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-2773">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2773">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-2774">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2774">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2775">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2775">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2776">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2776">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2777">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2777">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2778">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2778">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2780">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2780">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-2781">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2781">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2782">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2782">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2783">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2783">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-2784">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2785">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2786">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2787">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2787">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2788">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2789">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2790">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2791">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2792">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2793">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2794">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2795">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2796">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2796">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2798">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2798">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2799">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2799">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2800">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2800">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-2801">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2801">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-2802">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2802">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-2803">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2803">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-2804">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2804">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2806">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2807">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2807">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-2808">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2808">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-2809">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2809">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2811">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="a2762-2812">DXGI_FORMAT_D32 \_ float<sup></sup> -Zeichen (40)</span><span class="sxs-lookup"><span data-stu-id="a2762-2812">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="a2762-2813">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2813">Target</span></span> | <span data-ttu-id="a2762-2814">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2815">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2816">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2816">32</span></span> |
| <span data-ttu-id="a2762-2817">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2817">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2819">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2820">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2821">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2822">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2823">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2825">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2827">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-2828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2828">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2830">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2830">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-2831">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2831">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-2832">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2833">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2834">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2835">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2836">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2836">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2838">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2840">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2841">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-2842">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2842">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2844">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2845">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2846">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2846">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2847">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2848">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2849">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2850">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2851">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2852">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2853">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2854">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2855">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2855">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2857">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2857">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2859">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2859">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2861">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2861">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2863">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2863">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-2864">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2864">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-2865">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2865">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-2866">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2866">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2868">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2868">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2869">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2869">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-2870">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2870">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-2871">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2871">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2873">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="a2762-2874">DXGI_FORMAT_R32 \_ float<sup></sup> -Zeichen (41)</span><span class="sxs-lookup"><span data-stu-id="a2762-2874">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="a2762-2875">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2875">Target</span></span> | <span data-ttu-id="a2762-2876">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2876">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2877">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2878">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2878">32</span></span> |
| <span data-ttu-id="a2762-2879">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2879">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2881">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2881">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2883">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2883">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2885">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-2886">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2886">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2888">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2888">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2890">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2892">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2892">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2894">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2894">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2896">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2896">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2898">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2898">Shader sample (any filter)</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2900">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2900">Shader sample\_c (comparison filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2902">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2902">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2903">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2903">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2904">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2904">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2905">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2905">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2907">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2907">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2909">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2911">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2911">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2913">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2913">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-2914">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2914">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2915">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2915">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2916">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2916">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2917">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2917">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2918">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2918">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2919">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2919">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2920">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2920">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2921">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2921">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2922">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2922">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2923">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2923">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2924">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2924">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2925">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2925">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2926">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2926">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2928">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2928">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2930">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2930">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2932">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-2932">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2934">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-2934">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2936">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2936">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2938">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-2938">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-2939">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-2939">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2941">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-2941">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-2942">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2942">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-2943">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-2943">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-2944">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2944">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2946">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-2946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="a2762-2947">DXGI_FORMAT_R32 \_ uint-<sup>f</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="a2762-2947">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="a2762-2948">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2948">Target</span></span> | <span data-ttu-id="a2762-2949">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-2949">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-2950">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-2950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-2951">32</span><span class="sxs-lookup"><span data-stu-id="a2762-2951">32</span></span> |
| <span data-ttu-id="a2762-2952">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-2952">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2954">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2954">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2956">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-2956">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2958">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-2958">Input Assembler Index Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2960">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-2960">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-2962">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2964">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-2964">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2966">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-2966">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2968">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-2968">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2970">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-2970">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2972">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2972">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-2973">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2973">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-2974">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-2974">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-2975">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-2975">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-2976">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-2976">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-2977">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2977">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2979">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-2979">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-2980">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2980">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2982">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-2983">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-2983">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-2985">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-2985">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-2986">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2986">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2987">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-2987">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-2988">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-2988">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-2989">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-2989">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-2990">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-2990">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-2991">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-2991">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-2992">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-2992">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-2993">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-2993">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-2994">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-2994">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-2995">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-2995">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2996">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-2996">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-2997">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-2997">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-2999">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-2999">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3001">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3001">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3003">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3003">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3005">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-3006">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3006">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3008">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3009">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3009">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3011">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3011">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3012">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3012">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3013">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3013">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3014">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3014">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3016">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3016">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="a2762-3017">DXGI_FORMAT_R32 \_ Sint<sup></sup> -Werte (43)</span><span class="sxs-lookup"><span data-stu-id="a2762-3017">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="a2762-3018">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3018">Target</span></span> | <span data-ttu-id="a2762-3019">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3019">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3020">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3020">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3021">32</span><span class="sxs-lookup"><span data-stu-id="a2762-3021">32</span></span> |
| <span data-ttu-id="a2762-3022">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3022">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3024">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3024">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3026">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3026">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3028">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3029">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3029">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3031">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3031">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3033">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3033">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3035">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3035">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3037">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3037">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3039">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3039">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3041">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3041">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-3042">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3042">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3043">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3043">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3044">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3044">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3045">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3045">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3046">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3046">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3048">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3048">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-3049">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3049">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3051">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3051">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3052">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3052">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3053">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3053">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3054">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3054">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3055">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3055">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3056">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3056">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3057">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3057">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3058">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3058">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3059">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3059">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3060">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3060">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3061">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3061">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3062">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3062">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3063">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3063">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3064">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3064">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3065">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3065">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3067">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3067">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3069">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3069">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3071">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3071">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3073">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3073">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-3074">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3074">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3076">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3076">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3077">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3077">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3079">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3079">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3080">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3080">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3081">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3081">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3082">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3082">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3084">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3084">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="a2762-3085">DXGI_FORMAT_R24G8 \_ Typen losen<sup>PCs</sup> (44)</span><span class="sxs-lookup"><span data-stu-id="a2762-3085">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="a2762-3086">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3086">Target</span></span> | <span data-ttu-id="a2762-3087">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3087">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3088">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3088">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3089">32</span><span class="sxs-lookup"><span data-stu-id="a2762-3089">32</span></span> |
| <span data-ttu-id="a2762-3090">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3090">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3092">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3092">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3093">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3093">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3094">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3094">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3095">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3095">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3096">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3096">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3098">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3098">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3100">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3100">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-3101">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3101">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3103">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3103">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-3104">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-3105">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3106">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3107">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3107">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3108">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3109">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3109">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3111">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3111">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-3112">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3112">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3113">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3113">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3114">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3115">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3116">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3117">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3118">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3118">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3119">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3120">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3121">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3122">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3123">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3124">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3125">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3126">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3127">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3127">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3129">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3130">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3131">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-3132">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-3133">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3133">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-3134">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3135">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3135">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3137">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3138">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3139">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3140">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3140">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-3141">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3141">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="a2762-3142">DXGI_FORMAT_D24 \_ unorm \_ S8 \_ uint<sup></sup> -Zeichen (45)</span><span class="sxs-lookup"><span data-stu-id="a2762-3142">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="a2762-3143">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3143">Target</span></span> | <span data-ttu-id="a2762-3144">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3144">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3145">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3145">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3146">32</span><span class="sxs-lookup"><span data-stu-id="a2762-3146">32</span></span> |
| <span data-ttu-id="a2762-3147">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3147">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3149">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3149">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3150">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3150">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3151">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3151">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3152">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3152">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3153">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3153">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3155">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3157">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-3158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3158">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3160">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3160">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-3161">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-3162">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3163">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3164">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3164">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3165">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3166">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3166">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3168">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3168">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-3169">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3169">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3170">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3170">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3171">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3171">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3172">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3172">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3174">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3174">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3175">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3175">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3176">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3176">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3177">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3177">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3178">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3178">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3179">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3179">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3180">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3180">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3181">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3181">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3182">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3182">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3183">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3183">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3184">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3184">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3185">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3185">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3187">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3187">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3189">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3189">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3191">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3191">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3193">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3193">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-3194">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3194">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-3195">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3195">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3196">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3196">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3198">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3198">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3199">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3199">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3200">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3200">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3201">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3201">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-3202">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3202">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="a2762-3203">DXGI_FORMAT_R24 \_ unorm \_ X8- \_ typlosen<sup>f</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="a2762-3203">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="a2762-3204">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3204">Target</span></span> | <span data-ttu-id="a2762-3205">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3205">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3206">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3206">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3207">32</span><span class="sxs-lookup"><span data-stu-id="a2762-3207">32</span></span> |
| <span data-ttu-id="a2762-3208">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3208">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3210">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3210">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3211">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3211">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3212">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3212">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3213">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3213">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3214">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3214">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3216">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3218">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-3219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3219">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3221">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3221">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3223">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3223">Shader sample (any filter)</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3225">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3225">Shader sample\_c (comparison filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3227">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3227">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3228">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3228">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3229">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3229">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3230">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3230">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3232">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3232">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-3233">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3233">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3234">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3234">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3235">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3235">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3236">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3236">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3237">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3237">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3238">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3238">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3239">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3239">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3240">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3240">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3241">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3241">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3242">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3242">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3243">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3243">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3244">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3244">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3245">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3245">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3246">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3246">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3247">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3247">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3248">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3248">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3250">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3250">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3251">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3251">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3252">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3252">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-3253">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3253">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-3254">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3254">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-3255">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3255">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3256">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3256">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3258">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3258">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3259">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3259">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3260">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3260">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3261">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3261">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-3262">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3262">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="a2762-3263">DXGI_FORMAT_X24 \_ typlose \_ G8 \_ uint<sup></sup> -Zeichen (47)</span><span class="sxs-lookup"><span data-stu-id="a2762-3263">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="a2762-3264">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3264">Target</span></span> | <span data-ttu-id="a2762-3265">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3265">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3266">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3266">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3267">32</span><span class="sxs-lookup"><span data-stu-id="a2762-3267">32</span></span> |
| <span data-ttu-id="a2762-3268">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3268">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3270">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3270">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3271">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3271">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3272">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3272">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3273">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3273">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3274">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3274">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3276">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3276">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3278">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3278">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-3279">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3279">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3281">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3281">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3283">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3283">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-3284">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3284">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3285">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3285">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3286">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3286">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3287">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3287">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3288">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3288">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3290">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3290">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-3291">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3291">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3292">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3292">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3293">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3293">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3294">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3294">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3295">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3295">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3296">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3296">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3297">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3297">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3298">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3298">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3299">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3299">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3300">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3300">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3301">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3301">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3302">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3302">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3303">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3303">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3304">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3304">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3305">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3305">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3306">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3306">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3308">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3308">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3309">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3309">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3310">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3310">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-3311">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3311">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-3312">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3312">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-3313">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3313">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3314">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3314">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3316">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3316">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3317">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3317">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3318">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3318">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3319">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3319">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-3320">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3320">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="a2762-3321">DXGI_FORMAT_R8G8 \_ Typen losen<sup>PCs</sup> (48)</span><span class="sxs-lookup"><span data-stu-id="a2762-3321">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="a2762-3322">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3322">Target</span></span> | <span data-ttu-id="a2762-3323">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3323">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3324">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3324">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3325">16</span><span class="sxs-lookup"><span data-stu-id="a2762-3325">16</span></span> |
| <span data-ttu-id="a2762-3326">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3326">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3328">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3328">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3329">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3329">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3330">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3330">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3331">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3331">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3332">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3332">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3334">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3336">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3336">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3338">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3338">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3340">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3340">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-3341">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3341">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-3342">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3342">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3343">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3343">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3344">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3344">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3345">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3345">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3346">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3346">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3348">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3348">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-3349">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3349">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3350">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3350">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3351">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3351">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3352">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3352">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3353">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3353">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3354">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3354">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3355">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3355">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3356">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3356">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3357">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3357">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3358">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3358">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3359">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3359">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3360">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3360">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3361">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3361">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3362">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3362">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3363">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3363">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3364">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3364">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3366">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3366">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3367">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3367">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3368">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3368">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-3369">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-3370">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3370">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-3371">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3372">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3372">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3374">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3375">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3376">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3377">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3377">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-3378">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="a2762-3379">DXGI_FORMAT_R8G8 \_ unorm-Datei-<sup>e</sup> /a (49)</span><span class="sxs-lookup"><span data-stu-id="a2762-3379">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="a2762-3380">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3380">Target</span></span> | <span data-ttu-id="a2762-3381">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3381">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3382">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3383">16</span><span class="sxs-lookup"><span data-stu-id="a2762-3383">16</span></span> |
| <span data-ttu-id="a2762-3384">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3384">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3386">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3386">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3388">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3388">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3390">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3390">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3391">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3391">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3392">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3392">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3394">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3394">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3396">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3396">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3398">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3400">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3400">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3402">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3402">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3404">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3404">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3405">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3405">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3406">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3406">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3407">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3407">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3408">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3408">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3410">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3410">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3412">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3414">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3414">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3416">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3416">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3417">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3417">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3418">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3418">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3419">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3419">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3420">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3420">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3421">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3421">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3422">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3422">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3423">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3423">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3424">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3424">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3425">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3425">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3426">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3426">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3427">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3427">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3428">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3428">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3429">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3429">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3431">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3431">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3433">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3433">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3435">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3435">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3437">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3437">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3439">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3439">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3441">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3442">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3442">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3444">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3444">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3445">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3445">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3446">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3446">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3447">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3447">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3449">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="a2762-3450">DXGI_FORMAT_R8G8 \_ uint-<sup>f</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="a2762-3450">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="a2762-3451">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3451">Target</span></span> | <span data-ttu-id="a2762-3452">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3452">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3453">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3454">16</span><span class="sxs-lookup"><span data-stu-id="a2762-3454">16</span></span> |
| <span data-ttu-id="a2762-3455">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3455">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3457">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3457">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3459">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3459">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3461">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3461">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3462">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3462">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3463">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3463">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3465">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3465">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3467">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3467">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3469">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3469">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3471">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3471">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3473">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3473">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-3474">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3474">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3475">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3475">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3476">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3476">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3477">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3477">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3478">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3478">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3480">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3480">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-3481">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3481">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3483">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3483">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3484">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3484">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3486">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3486">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3487">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3487">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3488">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3488">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3489">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3489">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3490">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3490">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3491">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3491">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3492">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3492">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3493">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3493">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3494">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3494">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3495">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3495">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3496">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3496">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3497">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3497">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3498">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3498">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3500">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3500">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3502">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3502">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3504">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3504">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3506">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-3507">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3507">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3509">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3509">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3510">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3510">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3512">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3512">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3513">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3513">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3514">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3514">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3515">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3515">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-3516">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3516">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="a2762-3517">DXGI_FORMAT_R8G8 \_ snorm<sup></sup> -snorm (51)</span><span class="sxs-lookup"><span data-stu-id="a2762-3517">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="a2762-3518">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3518">Target</span></span> | <span data-ttu-id="a2762-3519">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3519">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3520">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3520">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3521">16</span><span class="sxs-lookup"><span data-stu-id="a2762-3521">16</span></span> |
| <span data-ttu-id="a2762-3522">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3522">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3524">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3524">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3526">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3526">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3528">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3529">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3530">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3532">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3532">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3534">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3534">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3536">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3536">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3538">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3538">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3540">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3540">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3542">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3542">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3543">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3543">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3544">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3544">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3545">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3545">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3546">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3546">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3548">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3548">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3550">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3550">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3552">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3552">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3553">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3553">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3554">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3554">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3555">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3555">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3556">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3556">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3557">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3557">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3558">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3558">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3559">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3559">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3560">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3560">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3561">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3561">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3562">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3562">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3563">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3563">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3564">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3564">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3565">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3565">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3566">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3566">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3568">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3568">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3570">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3570">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3572">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3572">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3574">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3574">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3576">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3576">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3578">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3579">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3579">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3581">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3582">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3583">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3584">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3584">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-3585">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="a2762-3586">DXGI_FORMAT_R8G8 \_ Sint<sup></sup> -Werte (52)</span><span class="sxs-lookup"><span data-stu-id="a2762-3586">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="a2762-3587">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3587">Target</span></span> | <span data-ttu-id="a2762-3588">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3588">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3589">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3590">16</span><span class="sxs-lookup"><span data-stu-id="a2762-3590">16</span></span> |
| <span data-ttu-id="a2762-3591">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3591">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3593">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3593">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3595">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3595">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3597">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3598">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3599">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3601">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3603">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3605">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3607">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3607">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3609">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-3610">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3611">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3612">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3612">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3613">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3614">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3614">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3616">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3617">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3619">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3619">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3620">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3620">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3621">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3621">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3622">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3622">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3623">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3623">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3624">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3624">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3625">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3625">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3626">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3626">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3627">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3627">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3628">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3628">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3629">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3629">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3630">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3630">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3631">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3631">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3632">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3632">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3633">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3633">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3635">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3635">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3637">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3637">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3639">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3639">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3641">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-3642">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3642">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3644">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3645">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3645">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3647">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3647">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3648">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3648">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3649">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3649">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3650">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3650">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-3651">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3651">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="a2762-3652">DXGI_FORMAT_R16 \_ Typen losen<sup>PCs</sup> (53)</span><span class="sxs-lookup"><span data-stu-id="a2762-3652">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="a2762-3653">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3653">Target</span></span> | <span data-ttu-id="a2762-3654">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3654">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3655">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3655">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3656">16</span><span class="sxs-lookup"><span data-stu-id="a2762-3656">16</span></span> |
| <span data-ttu-id="a2762-3657">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3657">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3659">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3659">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3660">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3660">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3661">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3661">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3662">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3662">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3663">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3663">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3665">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3667">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3667">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3669">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3669">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3671">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3671">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-3672">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3672">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-3673">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3673">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3674">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3674">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3675">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3675">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3676">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3676">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3677">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3677">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3679">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3679">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-3680">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3680">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3681">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3681">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3682">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3682">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3683">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3683">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3684">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3684">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3685">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3685">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3686">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3686">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3687">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3687">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3688">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3688">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3689">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3689">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3690">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3690">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3691">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3691">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3692">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3692">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3693">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3693">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3694">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3694">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3695">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3695">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3697">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3697">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3698">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3698">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3699">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3699">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-3700">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3700">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-3701">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3701">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-3702">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3702">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3703">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3703">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3705">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3706">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3707">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3708">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3708">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3710">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="a2762-3711">DXGI_FORMAT_R16 \_ float<sup></sup> -Zeichen (54)</span><span class="sxs-lookup"><span data-stu-id="a2762-3711">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="a2762-3712">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3712">Target</span></span> | <span data-ttu-id="a2762-3713">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3713">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3714">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3715">16</span><span class="sxs-lookup"><span data-stu-id="a2762-3715">16</span></span> |
| <span data-ttu-id="a2762-3716">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3716">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3718">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3718">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3720">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3720">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3722">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3722">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3723">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3723">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3724">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3724">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3726">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3728">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3730">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3732">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3732">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3734">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3734">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3736">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3737">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3738">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3738">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3739">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3740">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3740">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3742">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3742">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3744">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3746">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3746">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3748">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3749">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3750">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3751">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3752">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3752">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3753">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3754">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3755">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3756">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3757">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3757">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3758">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3759">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3760">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3761">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3761">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3763">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3763">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3765">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3765">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3767">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3767">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3769">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3769">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3771">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3771">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3773">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3773">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3774">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3774">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3776">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3777">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3778">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3779">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3779">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3781">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3781">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="a2762-3782">DXGI_FORMAT_D16 \_ unorm-Datei-<sup>e</sup> /a (55)</span><span class="sxs-lookup"><span data-stu-id="a2762-3782">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="a2762-3783">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3783">Target</span></span> | <span data-ttu-id="a2762-3784">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3784">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3785">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3785">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3786">16</span><span class="sxs-lookup"><span data-stu-id="a2762-3786">16</span></span> |
| <span data-ttu-id="a2762-3787">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3787">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3789">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3789">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3790">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3790">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3791">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3792">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3793">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3795">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3797">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-3798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3798">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3800">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3800">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-3801">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3801">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-3802">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3803">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3804">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3804">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3805">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3806">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3806">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3808">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-3809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3809">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3810">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3811">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3812">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3812">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3814">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3814">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3815">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3815">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3816">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3816">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3817">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3817">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3818">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3818">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3819">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3819">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3820">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3820">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3821">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3821">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3822">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3822">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3823">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3823">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3824">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3824">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3825">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3825">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3827">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3827">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3829">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3829">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3831">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3831">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3833">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-3834">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3834">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-3835">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3836">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3836">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3838">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3838">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3839">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3839">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3840">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3841">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3841">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3843">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3843">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="a2762-3844">DXGI_FORMAT_R16 \_ unorm-Datei-<sup>e</sup> /a (56)</span><span class="sxs-lookup"><span data-stu-id="a2762-3844">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="a2762-3845">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3845">Target</span></span> | <span data-ttu-id="a2762-3846">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3846">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3847">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3847">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3848">16</span><span class="sxs-lookup"><span data-stu-id="a2762-3848">16</span></span> |
| <span data-ttu-id="a2762-3849">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3849">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3851">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3851">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3853">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3853">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3855">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3855">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3856">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3856">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3857">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3857">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3859">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3859">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3861">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3861">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3863">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3863">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3865">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3865">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3867">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3867">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3869">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3869">Shader sample\_c (comparison filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3871">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3871">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3872">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3872">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3873">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3873">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3874">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3874">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3876">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3876">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3878">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3878">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3880">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3880">Blendable RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3882">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3882">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-3883">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3883">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3884">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3884">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3885">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3885">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3886">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3886">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3887">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3887">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3888">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3888">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3889">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3889">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3890">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3890">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3891">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3891">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3892">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3892">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3893">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3893">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3894">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3894">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3895">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3895">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3897">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3897">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3899">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3899">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3901">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3901">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3903">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3903">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3905">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3905">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3907">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3907">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3908">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3908">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3910">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3910">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3911">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3911">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3912">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3912">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3913">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3913">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3915">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3915">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="a2762-3916">DXGI_FORMAT_R16 \_ uint-<sup>f</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="a2762-3916">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="a2762-3917">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3917">Target</span></span> | <span data-ttu-id="a2762-3918">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3918">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3919">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3919">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3920">16</span><span class="sxs-lookup"><span data-stu-id="a2762-3920">16</span></span> |
| <span data-ttu-id="a2762-3921">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3921">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3923">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3923">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3925">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3925">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3927">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3927">Input Assembler Index Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3929">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3929">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3930">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3930">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-3932">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-3934">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3936">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-3936">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3938">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-3938">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3940">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3940">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-3941">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3941">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-3942">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-3942">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-3943">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-3943">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-3944">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-3944">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-3945">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3945">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3947">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-3947">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-3948">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3948">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3950">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-3951">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-3951">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3953">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3953">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-3954">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3954">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3955">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-3955">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-3956">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-3956">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-3957">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-3957">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-3958">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3958">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-3959">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-3959">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-3960">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-3960">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-3961">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-3961">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-3962">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-3962">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-3963">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-3963">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3964">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-3964">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-3965">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-3965">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3967">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3967">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3969">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-3969">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3971">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-3971">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3973">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-3973">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-3974">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-3974">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-3976">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-3976">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-3977">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-3977">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3979">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-3979">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-3980">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3980">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-3981">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-3981">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-3982">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3982">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3984">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-3984">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="a2762-3985">DXGI_FORMAT_R16 \_ snorm<sup></sup> -snorm (58)</span><span class="sxs-lookup"><span data-stu-id="a2762-3985">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="a2762-3986">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-3986">Target</span></span> | <span data-ttu-id="a2762-3987">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-3987">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-3988">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-3988">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-3989">16</span><span class="sxs-lookup"><span data-stu-id="a2762-3989">16</span></span> |
| <span data-ttu-id="a2762-3990">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-3990">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3992">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3992">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3994">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-3994">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-3996">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-3996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3997">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-3997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-3998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-3998">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4000">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4002">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4002">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4004">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4004">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4006">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4006">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4008">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4008">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4010">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4010">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4011">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4011">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4012">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4012">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4013">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4013">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4014">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4014">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4016">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4016">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4018">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4018">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4020">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4020">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4021">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4021">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4022">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4022">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4023">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4023">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4024">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4024">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4025">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4025">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4026">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4026">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4027">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4027">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4028">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4028">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4029">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4029">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4030">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4030">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4031">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4031">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4032">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4032">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4033">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4033">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4034">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4034">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4036">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4036">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4038">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4038">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4040">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4040">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4042">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4042">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4044">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4044">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4046">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4046">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4047">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4047">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4049">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4050">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4051">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4052">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4052">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4054">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4054">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="a2762-4055">DXGI_FORMAT_R16 \_ Sint<sup></sup> -Werte (59)</span><span class="sxs-lookup"><span data-stu-id="a2762-4055">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="a2762-4056">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4056">Target</span></span> | <span data-ttu-id="a2762-4057">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4057">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4058">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4058">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4059">16</span><span class="sxs-lookup"><span data-stu-id="a2762-4059">16</span></span> |
| <span data-ttu-id="a2762-4060">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4060">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4062">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4062">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4064">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4064">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4066">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4066">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4067">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4067">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4068">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4068">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4070">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4072">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4074">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4076">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4076">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4078">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4078">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-4079">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4079">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4080">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4080">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4081">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4081">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4082">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4082">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4083">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4083">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4085">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4085">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-4086">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4086">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4088">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4089">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4090">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4091">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4092">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4093">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4093">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4094">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4095">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4096">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4097">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4098">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4098">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4099">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4100">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4101">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4102">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4102">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4104">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4104">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4106">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4106">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4108">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4108">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4110">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4110">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-4111">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4111">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4113">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4113">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4114">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4114">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4116">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4116">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4117">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4117">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4118">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4118">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4119">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4119">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4121">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4121">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="a2762-4122">DXGI_FORMAT_R8 \_ Typen losen<sup>PCs</sup> (60)</span><span class="sxs-lookup"><span data-stu-id="a2762-4122">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="a2762-4123">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4123">Target</span></span> | <span data-ttu-id="a2762-4124">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4124">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4125">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4125">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4126">8</span><span class="sxs-lookup"><span data-stu-id="a2762-4126">8</span></span> |
| <span data-ttu-id="a2762-4127">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4127">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4129">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4129">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4130">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4131">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4132">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4133">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4135">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4137">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4137">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4139">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4141">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4141">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-4142">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4142">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-4143">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4143">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4144">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4144">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4145">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4145">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4146">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4146">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4147">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4147">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4149">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4149">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-4150">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4150">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4151">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4151">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4152">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4152">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4153">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4153">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4154">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4154">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4155">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4155">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4156">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4156">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4157">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4157">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4158">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4158">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4159">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4159">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4160">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4160">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4161">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4161">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4162">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4162">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4163">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4163">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4164">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4164">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4165">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4165">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4167">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4167">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4168">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4168">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4169">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4169">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-4170">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4170">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-4171">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4171">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-4172">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4172">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4173">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4173">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4175">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4175">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4176">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4176">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4177">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4177">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4178">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4178">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4180">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4180">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="a2762-4181">DXGI_FORMAT_R8 \_ unorm-Datei-<sup>e</sup> /a (61)</span><span class="sxs-lookup"><span data-stu-id="a2762-4181">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="a2762-4182">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4182">Target</span></span> | <span data-ttu-id="a2762-4183">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4183">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4184">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4184">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4185">8</span><span class="sxs-lookup"><span data-stu-id="a2762-4185">8</span></span> |
| <span data-ttu-id="a2762-4186">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4186">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4188">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4188">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4190">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4190">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4192">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4193">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4194">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4196">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4196">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4198">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4198">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4200">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4202">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4202">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4204">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4204">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4206">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4207">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4208">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4209">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4210">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4210">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4212">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4212">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4214">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4214">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4216">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4216">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4218">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4218">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4219">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4219">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4220">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4220">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4221">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4221">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4222">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4222">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4223">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4223">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4224">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4224">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4225">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4225">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4226">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4226">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4227">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4227">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4228">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4228">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4229">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4229">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4230">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4230">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4231">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4231">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4233">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4233">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4235">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4235">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4237">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4237">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4239">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4239">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4241">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4241">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4243">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4243">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4244">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4244">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4246">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4246">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4247">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4247">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4248">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4248">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4249">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4249">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4251">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="a2762-4252">DXGI_FORMAT_R8 \_ uint-<sup>f</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="a2762-4252">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="a2762-4253">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4253">Target</span></span> | <span data-ttu-id="a2762-4254">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4254">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4255">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4256">8</span><span class="sxs-lookup"><span data-stu-id="a2762-4256">8</span></span> |
| <span data-ttu-id="a2762-4257">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4257">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4259">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4259">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4261">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4261">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4263">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4264">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4265">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4267">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4269">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4271">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4271">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4273">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4273">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4275">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4275">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-4276">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4276">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4277">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4277">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4278">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4278">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4279">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4279">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4280">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4280">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4282">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4282">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-4283">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4283">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4285">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4286">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4286">Output Merger Logic Op</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4288">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4288">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4289">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4289">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4290">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4290">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4291">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4291">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4292">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4292">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4293">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4293">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4294">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4294">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4295">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4295">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4296">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4296">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4297">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4297">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4298">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4298">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4299">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4299">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4300">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4300">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4302">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4302">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4304">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4304">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4306">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4306">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4308">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4308">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-4309">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4309">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4311">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4311">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4312">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4312">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4314">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4314">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4315">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4315">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4316">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4316">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4317">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4317">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4319">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4319">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="a2762-4320">DXGI_FORMAT_R8 \_ snorm<sup></sup> -snorm (63)</span><span class="sxs-lookup"><span data-stu-id="a2762-4320">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="a2762-4321">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4321">Target</span></span> | <span data-ttu-id="a2762-4322">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4322">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4323">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4323">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4324">8</span><span class="sxs-lookup"><span data-stu-id="a2762-4324">8</span></span> |
| <span data-ttu-id="a2762-4325">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4325">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4327">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4327">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4329">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4329">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4331">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4332">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4333">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4335">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4335">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4337">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4337">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4339">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4339">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4341">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4341">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4343">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4343">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4345">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4346">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4347">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4347">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4348">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4349">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4349">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4351">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4351">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4353">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4353">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4355">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4355">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4356">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4356">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4357">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4357">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4358">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4358">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4359">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4359">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4360">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4360">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4361">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4361">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4362">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4362">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4363">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4363">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4364">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4364">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4365">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4365">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4366">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4366">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4367">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4367">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4368">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4368">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4369">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4369">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4371">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4371">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4373">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4373">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4375">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4375">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4377">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4377">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4379">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4379">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4381">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4382">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4382">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4384">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4385">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4386">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4387">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4387">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4389">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="a2762-4390">DXGI_FORMAT_R8 \_ Sint<sup></sup> -Werte (64)</span><span class="sxs-lookup"><span data-stu-id="a2762-4390">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="a2762-4391">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4391">Target</span></span> | <span data-ttu-id="a2762-4392">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4392">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4393">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4394">8</span><span class="sxs-lookup"><span data-stu-id="a2762-4394">8</span></span> |
| <span data-ttu-id="a2762-4395">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4395">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4397">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4397">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4399">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4399">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4401">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4402">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4403">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4405">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4405">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4407">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4407">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4409">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4409">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4411">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4411">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4413">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-4414">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4415">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4416">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4416">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4417">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4418">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4418">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4420">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4420">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-4421">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4421">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4423">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4424">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4425">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4426">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4427">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4428">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4429">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4430">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4431">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4432">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4433">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4433">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4434">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4435">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4436">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4437">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4437">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4439">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4439">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4441">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4441">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4443">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4443">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4445">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4445">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-4446">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4446">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4448">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4448">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4449">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4449">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4451">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4451">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4452">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4452">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4453">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4453">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4454">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4454">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4456">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="a2762-4457">DXGI_FORMAT_A8 \_ unorm<sup></sup> -Fehler (65)</span><span class="sxs-lookup"><span data-stu-id="a2762-4457">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="a2762-4458">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4458">Target</span></span> | <span data-ttu-id="a2762-4459">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4459">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4460">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4461">8</span><span class="sxs-lookup"><span data-stu-id="a2762-4461">8</span></span> |
| <span data-ttu-id="a2762-4462">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4462">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4464">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4464">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4465">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4466">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4467">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4468">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4470">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4470">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4472">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4472">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4474">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4474">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4476">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4476">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4478">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4478">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4480">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4480">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4481">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4481">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4482">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4482">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4483">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4483">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4484">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4484">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4486">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4486">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4488">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4488">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4490">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4490">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4492">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4492">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4493">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4493">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4494">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4494">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4495">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4495">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4496">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4496">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4497">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4497">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4498">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4498">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4499">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4499">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4500">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4500">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4501">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4501">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4502">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4502">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4503">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4503">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4504">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4504">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4505">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4505">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4507">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4507">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4509">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4509">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4511">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4511">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4513">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4513">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4515">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4515">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-4517">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4517">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4518">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4518">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-4519">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4519">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4520">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4520">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4521">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4521">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4522">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4522">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4524">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4524">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="a2762-4525">DXGI_FORMAT_R9G9B9E5 \_ sharede XP-<sup>LNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="a2762-4525">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="a2762-4526">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4526">Target</span></span> | <span data-ttu-id="a2762-4527">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4527">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4528">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4528">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4529">32</span><span class="sxs-lookup"><span data-stu-id="a2762-4529">32</span></span> |
| <span data-ttu-id="a2762-4530">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4530">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4532">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4532">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4533">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4533">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4534">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4534">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4535">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4535">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4536">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4536">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4538">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4538">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4540">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4540">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4542">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4542">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4544">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4544">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4546">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4546">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4548">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4548">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4549">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4549">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4550">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4550">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4551">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4551">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4552">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4552">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4554">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4554">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-4555">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4555">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4556">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4556">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4557">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4557">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4558">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4558">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4559">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4559">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4560">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4560">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4561">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4561">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4562">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4562">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4563">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4563">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4564">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4564">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4565">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4565">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4566">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4566">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4567">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4567">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4568">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4568">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4569">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4569">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4570">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4570">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4572">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4572">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4573">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4573">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4574">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4574">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-4575">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4575">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-4576">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4576">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-4577">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4577">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4578">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4578">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-4579">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4579">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4580">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4580">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4581">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4581">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4582">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4582">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-4583">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4583">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="a2762-4584">DXGI_FORMAT_R8G8 \_ B8G8 \_ unorm<sup></sup> -Fehler (68)</span><span class="sxs-lookup"><span data-stu-id="a2762-4584">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="a2762-4585">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4585">Target</span></span> | <span data-ttu-id="a2762-4586">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4586">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4587">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4587">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4588">16</span><span class="sxs-lookup"><span data-stu-id="a2762-4588">16</span></span> |
| <span data-ttu-id="a2762-4589">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4589">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4591">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4591">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4592">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4592">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4593">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4593">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4594">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4594">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4595">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4595">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4597">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4597">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4599">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4599">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4601">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4601">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4603">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4603">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4605">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4605">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4607">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4607">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4608">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4608">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4609">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4609">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4610">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4610">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4611">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4611">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4613">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-4614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4614">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4615">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4616">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4617">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4618">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4619">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4620">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4620">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4621">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4622">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4623">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4624">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4625">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4626">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4627">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4628">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4629">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4629">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4631">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4632">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4633">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-4634">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-4635">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4635">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-4636">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4637">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-4638">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4638">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4639">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4639">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4640">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4640">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4641">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4641">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-4642">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4642">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="a2762-4643">DXGI_FORMAT_G8R8 \_ G8B8 \_ unorm<sup></sup> -Fehler (69)</span><span class="sxs-lookup"><span data-stu-id="a2762-4643">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="a2762-4644">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4644">Target</span></span> | <span data-ttu-id="a2762-4645">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4645">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4646">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4646">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4647">16</span><span class="sxs-lookup"><span data-stu-id="a2762-4647">16</span></span> |
| <span data-ttu-id="a2762-4648">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4648">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4650">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4650">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4651">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4651">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4652">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4653">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4654">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4656">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4658">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4658">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4660">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4660">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4662">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4662">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4664">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4664">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4666">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4666">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4667">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4667">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4668">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4668">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4669">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4669">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4670">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4670">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4672">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-4673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4673">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4674">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4675">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4676">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4677">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4678">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4679">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4679">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4680">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4681">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4682">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4683">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4684">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4684">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4685">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4686">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4687">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4688">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4688">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4690">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4690">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4691">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4691">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4692">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4692">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-4693">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4693">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-4694">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4694">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-4695">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4695">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4696">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4696">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-4697">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4697">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4698">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4698">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4699">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4699">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4700">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4700">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-4701">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="a2762-4702">DXGI_FORMAT_BC1 \_ typloses<sup>PCC</sup> (70)</span><span class="sxs-lookup"><span data-stu-id="a2762-4702">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="a2762-4703">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4703">Target</span></span> | <span data-ttu-id="a2762-4704">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4704">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4705">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4706">4</span><span class="sxs-lookup"><span data-stu-id="a2762-4706">4</span></span> |
| <span data-ttu-id="a2762-4707">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4707">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4709">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4709">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4710">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4711">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4712">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4713">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-4714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4714">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4716">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4718">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4718">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4720">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4720">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-4721">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4721">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-4722">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4722">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4723">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4723">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4724">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4724">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4725">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4725">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4726">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4726">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4728">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-4729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4729">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4730">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4731">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4732">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4733">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4734">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4735">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4735">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4736">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4737">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4738">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4739">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4740">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4740">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4741">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4742">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4743">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4744">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4744">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4746">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4747">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4748">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-4749">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-4750">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4750">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-4751">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4752">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4752">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4754">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4755">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4756">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4757">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4757">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4759">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4759">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="a2762-4760">DXGI_FORMAT_BC1 \_ unorm<sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="a2762-4760">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="a2762-4761">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4761">Target</span></span> | <span data-ttu-id="a2762-4762">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4762">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4763">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4763">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4764">4</span><span class="sxs-lookup"><span data-stu-id="a2762-4764">4</span></span> |
| <span data-ttu-id="a2762-4765">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4765">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4767">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4767">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4768">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4768">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4769">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4769">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4770">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4770">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4771">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4771">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-4772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4772">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4774">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4776">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4778">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4778">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4780">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4780">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4782">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4782">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4783">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4783">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4784">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4784">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4785">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4785">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4786">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4786">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4788">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4788">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-4789">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4789">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4790">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4790">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4791">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4791">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4792">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4792">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4793">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4793">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4794">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4794">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4795">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4795">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4796">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4796">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4797">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4797">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4798">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4798">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4799">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4799">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4800">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4800">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4801">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4801">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4802">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4802">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4803">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4803">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4804">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4804">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4806">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4806">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4807">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4807">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4808">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4808">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-4809">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4809">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-4810">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4810">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-4811">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4812">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4812">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4814">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4815">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4816">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4817">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4817">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4819">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="a2762-4820">DXGI_FORMAT_BC1 \_ unorm \_ sRGB<sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="a2762-4820">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="a2762-4821">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4821">Target</span></span> | <span data-ttu-id="a2762-4822">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4822">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4823">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4824">4</span><span class="sxs-lookup"><span data-stu-id="a2762-4824">4</span></span> |
| <span data-ttu-id="a2762-4825">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4825">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4827">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4827">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4828">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4829">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4830">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4831">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-4832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4832">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4834">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4836">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4836">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4838">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4838">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4840">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4840">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4842">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4842">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4843">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4843">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4844">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4844">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4845">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4845">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4846">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4846">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4848">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-4849">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4849">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4850">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4851">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4852">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4853">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4854">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4855">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4855">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4856">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4857">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4858">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4859">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4860">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4860">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4861">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4862">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4863">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4864">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4864">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4866">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4866">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4867">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4867">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4868">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4868">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-4869">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-4870">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4870">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-4871">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4872">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4872">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4874">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4875">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4876">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4877">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4877">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4879">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="a2762-4880">DXGI_FORMAT_BC2 \_ typloses<sup>PCC</sup> (73)</span><span class="sxs-lookup"><span data-stu-id="a2762-4880">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="a2762-4881">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4881">Target</span></span> | <span data-ttu-id="a2762-4882">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4882">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4883">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4884">8</span><span class="sxs-lookup"><span data-stu-id="a2762-4884">8</span></span> |
| <span data-ttu-id="a2762-4885">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4885">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4887">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4887">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4888">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4888">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4889">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4890">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4891">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-4892">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4892">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4894">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4894">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4896">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4896">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4898">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4898">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-4899">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4899">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-4900">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4900">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4901">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4901">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4902">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4902">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4903">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4903">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4904">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4904">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4906">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4906">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-4907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4907">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4908">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4908">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4909">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4909">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4910">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4910">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4911">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4911">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4912">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4912">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4913">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4913">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4914">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4914">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4915">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4915">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4916">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4916">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4917">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4917">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4918">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4918">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4919">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4919">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4920">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4920">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4921">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4921">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4922">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4922">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4924">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4924">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4925">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4925">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4926">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4926">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-4927">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4927">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-4928">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4928">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-4929">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4929">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4930">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4930">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4932">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4933">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4934">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4935">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4935">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4937">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="a2762-4938">DXGI_FORMAT_BC2 \_ unorm<sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="a2762-4938">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="a2762-4939">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4939">Target</span></span> | <span data-ttu-id="a2762-4940">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-4940">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-4941">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-4941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-4942">8</span><span class="sxs-lookup"><span data-stu-id="a2762-4942">8</span></span> |
| <span data-ttu-id="a2762-4943">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-4943">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4945">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4945">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4946">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-4946">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4947">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-4947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4948">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-4948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-4949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-4949">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-4950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-4950">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-4952">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4954">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-4954">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4956">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-4956">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4958">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4958">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4960">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4960">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-4961">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-4961">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-4962">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-4962">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-4963">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-4963">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-4964">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4964">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4966">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-4966">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-4967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4967">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4968">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4968">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4969">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-4969">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-4970">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4970">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-4971">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4971">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4972">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-4972">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-4973">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-4973">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-4974">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-4974">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-4975">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4975">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-4976">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-4976">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-4977">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-4977">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-4978">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-4978">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-4979">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-4979">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-4980">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-4980">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4981">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-4981">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-4982">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-4982">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4984">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4984">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4985">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-4985">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-4986">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-4986">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-4987">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-4987">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-4988">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-4988">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-4989">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-4989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-4990">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-4990">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4992">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-4992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-4993">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-4994">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-4994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-4995">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4995">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-4997">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-4997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="a2762-4998">DXGI_FORMAT_BC2 \_ unorm \_ sRGB<sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="a2762-4998">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="a2762-4999">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-4999">Target</span></span> | <span data-ttu-id="a2762-5000">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5000">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5001">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5002">8</span><span class="sxs-lookup"><span data-stu-id="a2762-5002">8</span></span> |
| <span data-ttu-id="a2762-5003">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5003">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5005">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5005">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5006">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5006">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5007">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5007">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5008">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5008">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5009">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5009">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-5010">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5010">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5012">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5012">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5014">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5014">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5016">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5016">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5018">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5018">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5020">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5020">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5021">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5021">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5022">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5022">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5023">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5023">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5024">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5024">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5026">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5026">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-5027">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5027">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5028">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5028">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5029">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5029">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5030">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5030">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5031">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5031">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5032">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5032">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5033">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5033">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5034">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5034">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5035">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5035">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5036">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5036">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5037">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5037">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5038">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5038">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5039">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5039">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5040">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5040">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5041">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5041">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5042">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5042">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5044">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5044">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5045">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5045">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5046">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5046">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-5047">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5047">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-5048">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5048">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-5049">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5049">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5050">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5050">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5052">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5052">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5053">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5053">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5054">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5054">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5055">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5055">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5057">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5057">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="a2762-5058">DXGI_FORMAT_BC3 \_ typloses<sup>PCC</sup> (76)</span><span class="sxs-lookup"><span data-stu-id="a2762-5058">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="a2762-5059">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5059">Target</span></span> | <span data-ttu-id="a2762-5060">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5060">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5061">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5061">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5062">8</span><span class="sxs-lookup"><span data-stu-id="a2762-5062">8</span></span> |
| <span data-ttu-id="a2762-5063">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5063">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5065">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5065">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5066">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5066">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5067">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5067">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5068">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5068">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5069">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5069">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-5070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5070">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5072">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5074">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5076">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5076">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-5077">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5077">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-5078">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5078">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5079">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5079">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5080">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5080">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5081">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5081">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5082">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5082">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5084">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5084">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-5085">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5085">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5086">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5087">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5088">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5089">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5090">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5091">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5091">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5092">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5093">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5094">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5095">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5096">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5096">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5097">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5098">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5099">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5100">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5100">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5102">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5102">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5103">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5103">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5104">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5104">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-5105">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5105">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-5106">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5106">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-5107">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5108">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5108">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5110">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5111">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5112">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5113">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5113">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5115">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="a2762-5116">DXGI_FORMAT_BC3 \_ unorm<sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="a2762-5116">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="a2762-5117">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5117">Target</span></span> | <span data-ttu-id="a2762-5118">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5118">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5119">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5120">8</span><span class="sxs-lookup"><span data-stu-id="a2762-5120">8</span></span> |
| <span data-ttu-id="a2762-5121">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5121">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5123">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5123">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5124">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5125">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5126">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5127">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-5128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5128">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5130">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5132">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5134">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5134">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5136">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5136">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5138">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5138">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5139">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5139">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5140">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5140">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5141">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5141">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5142">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5142">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5144">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-5145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5145">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5146">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5147">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5148">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5149">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5150">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5151">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5151">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5152">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5153">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5154">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5155">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5157">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5158">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5159">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5160">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5160">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5162">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5163">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5164">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-5165">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-5166">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5166">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-5167">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5168">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5168">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5170">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5170">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5171">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5171">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5172">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5172">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5173">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5173">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5175">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="a2762-5176">DXGI_FORMAT_BC3 \_ unorm \_ sRGB<sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="a2762-5176">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="a2762-5177">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5177">Target</span></span> | <span data-ttu-id="a2762-5178">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5178">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5179">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5180">8</span><span class="sxs-lookup"><span data-stu-id="a2762-5180">8</span></span> |
| <span data-ttu-id="a2762-5181">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5181">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5183">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5183">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5184">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5184">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5185">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5186">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5186">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5187">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-5188">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5188">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5190">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5190">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5192">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5192">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5194">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5194">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5196">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5196">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5198">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5198">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5199">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5199">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5200">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5200">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5201">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5201">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5202">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5202">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5204">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5204">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-5205">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5205">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5206">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5206">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5207">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5207">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5208">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5208">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5209">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5209">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5210">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5210">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5211">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5211">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5212">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5212">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5213">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5213">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5214">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5215">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5216">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5216">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5217">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5218">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5218">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5219">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5219">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5220">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5220">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5222">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5223">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5224">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-5225">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-5226">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5226">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-5227">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5228">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5228">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5230">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5230">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5231">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5231">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5232">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5232">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5233">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5233">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5235">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5235">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="a2762-5236">DXGI_FORMAT_BC4 \_ typloses<sup>PCC</sup> (79)</span><span class="sxs-lookup"><span data-stu-id="a2762-5236">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="a2762-5237">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5237">Target</span></span> | <span data-ttu-id="a2762-5238">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5238">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5239">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5239">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5240">4</span><span class="sxs-lookup"><span data-stu-id="a2762-5240">4</span></span> |
| <span data-ttu-id="a2762-5241">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5241">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5243">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5243">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5244">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5244">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5245">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5245">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5246">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5246">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5247">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-5248">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5248">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5250">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5250">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5252">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5254">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5254">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-5255">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5255">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-5256">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5256">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5257">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5257">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5258">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5258">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5259">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5259">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5260">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5260">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5262">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-5263">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5263">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5264">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5265">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5266">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5267">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5268">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5269">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5269">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5270">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5271">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5272">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5273">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5274">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5274">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5275">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5276">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5277">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5278">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5278">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5280">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5280">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5281">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5281">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5282">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5282">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-5283">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5283">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-5284">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5284">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-5285">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5285">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5286">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5286">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5288">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5289">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5290">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5291">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5291">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-5292">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="a2762-5293">DXGI_FORMAT_BC4 \_ unorm<sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="a2762-5293">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="a2762-5294">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5294">Target</span></span> | <span data-ttu-id="a2762-5295">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5295">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5296">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5297">4</span><span class="sxs-lookup"><span data-stu-id="a2762-5297">4</span></span> |
| <span data-ttu-id="a2762-5298">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5298">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5300">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5300">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5301">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5301">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5302">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5303">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5304">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-5305">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5305">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5307">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5307">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5309">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5309">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5311">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5311">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5313">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5313">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5315">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5316">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5317">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5317">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5318">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5319">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5319">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5321">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-5322">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5322">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5323">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5323">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5324">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5324">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5325">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5325">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5326">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5326">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5327">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5327">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5328">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5328">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5329">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5329">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5330">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5330">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5331">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5331">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5332">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5332">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5333">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5333">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5334">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5334">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5335">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5335">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5336">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5336">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5337">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5337">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5339">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5339">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5340">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5340">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5341">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5341">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-5342">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5342">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-5343">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5343">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-5344">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5345">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5345">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5347">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5348">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5349">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5350">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5350">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-5351">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5351">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="a2762-5352">DXGI_FORMAT_BC4 \_ snorm<sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="a2762-5352">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="a2762-5353">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5353">Target</span></span> | <span data-ttu-id="a2762-5354">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5354">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5355">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5355">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5356">4</span><span class="sxs-lookup"><span data-stu-id="a2762-5356">4</span></span> |
| <span data-ttu-id="a2762-5357">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5357">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5359">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5359">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5360">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5360">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5361">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5361">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5362">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5362">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5363">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5363">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-5364">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5364">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5366">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5366">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5368">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5368">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5370">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5370">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5372">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5372">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5374">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5375">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5376">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5376">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5377">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5378">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5378">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5380">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-5381">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5381">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5382">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5383">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5384">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5385">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5386">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5387">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5387">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5388">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5389">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5390">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5391">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5392">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5393">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5394">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5395">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5396">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5396">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5398">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5399">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5400">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-5401">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-5402">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5402">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-5403">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5404">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5404">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5406">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5407">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5408">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5409">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5409">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-5410">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="a2762-5411">DXGI_FORMAT_BC5 \_ typloses<sup>PCC</sup> (82)</span><span class="sxs-lookup"><span data-stu-id="a2762-5411">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="a2762-5412">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5412">Target</span></span> | <span data-ttu-id="a2762-5413">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5413">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5414">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5415">8</span><span class="sxs-lookup"><span data-stu-id="a2762-5415">8</span></span> |
| <span data-ttu-id="a2762-5416">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5416">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5418">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5418">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5419">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5419">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5420">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5420">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5421">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5421">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5422">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5422">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-5423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5423">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5425">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5427">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5429">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5429">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-5430">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5430">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-5431">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5431">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5432">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5432">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5433">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5433">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5434">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5434">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5435">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5435">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5437">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5437">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-5438">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5438">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5439">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5439">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5440">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5440">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5441">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5441">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5442">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5442">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5443">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5443">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5444">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5444">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5445">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5445">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5446">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5446">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5447">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5447">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5448">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5448">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5449">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5449">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5450">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5450">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5451">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5451">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5452">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5452">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5453">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5453">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5455">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5455">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5456">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5456">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5457">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5457">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-5458">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5458">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-5459">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5459">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-5460">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5460">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5461">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5461">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5463">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5463">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5464">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5464">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5465">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5465">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5466">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5466">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-5467">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5467">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="a2762-5468">DXGI_FORMAT_BC5 \_ unorm<sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="a2762-5468">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="a2762-5469">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5469">Target</span></span> | <span data-ttu-id="a2762-5470">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5470">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5471">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5471">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5472">8</span><span class="sxs-lookup"><span data-stu-id="a2762-5472">8</span></span> |
| <span data-ttu-id="a2762-5473">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5473">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5475">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5475">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5476">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5476">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5477">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5477">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5478">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5478">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5479">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5479">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-5480">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5480">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5482">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5482">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5484">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5484">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5486">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5486">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5488">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5488">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5490">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5490">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5491">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5491">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5492">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5492">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5493">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5493">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5494">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5494">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5496">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5496">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-5497">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5497">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5498">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5498">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5499">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5499">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5500">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5500">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5501">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5501">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5502">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5502">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5503">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5503">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5504">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5504">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5505">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5505">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5506">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5506">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5507">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5507">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5508">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5508">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5509">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5509">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5510">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5510">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5511">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5511">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5512">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5512">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5514">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5514">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5515">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5515">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5516">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5516">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-5517">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5517">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-5518">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5518">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-5519">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5520">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5520">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5522">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5523">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5524">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5525">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5525">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-5526">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="a2762-5527">DXGI_FORMAT_BC5 \_ snorm<sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="a2762-5527">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="a2762-5528">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5528">Target</span></span> | <span data-ttu-id="a2762-5529">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5529">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5530">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5531">8</span><span class="sxs-lookup"><span data-stu-id="a2762-5531">8</span></span> |
| <span data-ttu-id="a2762-5532">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5532">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5534">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5534">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5535">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5535">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5536">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5536">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5537">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5537">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5538">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5538">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-5539">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5539">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5541">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5541">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5543">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5545">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5545">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5547">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5547">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5549">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5549">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5550">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5550">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5551">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5551">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5552">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5552">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5553">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5553">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5555">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5555">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-5556">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5556">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5557">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5557">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5558">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5558">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5559">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5559">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5560">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5560">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5561">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5561">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5562">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5562">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5563">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5563">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5564">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5564">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5565">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5565">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5566">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5566">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5567">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5567">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5568">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5568">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5569">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5569">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5570">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5570">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5571">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5571">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5573">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5573">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5574">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5574">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5575">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5575">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-5576">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5576">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-5577">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5577">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-5578">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5579">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5579">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5581">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5582">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5583">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5584">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5584">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-5585">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="a2762-5586">DXGI_FORMAT_B5G6R5 \_ unorm<sup></sup> -Fehler (85)</span><span class="sxs-lookup"><span data-stu-id="a2762-5586">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="a2762-5587">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5587">Target</span></span> | <span data-ttu-id="a2762-5588">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5588">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5589">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5590">16</span><span class="sxs-lookup"><span data-stu-id="a2762-5590">16</span></span> |
| <span data-ttu-id="a2762-5591">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5591">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5593">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5593">Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5595">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5595">Input Assembler Vertex Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5597">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5598">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5599">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5601">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5603">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5605">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5607">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5607">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5609">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5609">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5611">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5612">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5613">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5613">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5614">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5615">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5615">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5617">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5617">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5619">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5621">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5621">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5623">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5623">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5624">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5624">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5625">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5625">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5626">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5626">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5627">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5627">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5628">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5628">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5629">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5629">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5630">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5630">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5631">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5631">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5632">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5632">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5633">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5633">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5634">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5634">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5635">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5635">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5636">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5636">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5638">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5638">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5640">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5640">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5642">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5642">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5644">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5644">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5646">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5646">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5648">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5648">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5649">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5649">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-5650">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5650">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5651">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5651">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5652">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5652">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5653">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5653">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-5654">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5654">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="a2762-5655">DXGI_FORMAT_B5G5R5A1 \_ unorm<sup></sup> -Fehler (86)</span><span class="sxs-lookup"><span data-stu-id="a2762-5655">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="a2762-5656">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5656">Target</span></span> | <span data-ttu-id="a2762-5657">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5657">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5658">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5658">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5659">16</span><span class="sxs-lookup"><span data-stu-id="a2762-5659">16</span></span> |
| <span data-ttu-id="a2762-5660">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5660">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5662">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5662">Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5664">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5664">Input Assembler Vertex Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5666">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5666">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5667">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5667">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5668">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5668">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5670">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5670">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5672">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5672">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5674">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5674">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5676">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5676">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5678">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5678">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5680">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5681">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5682">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5682">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5683">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5684">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5684">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5686">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5686">Mipmap Auto-Generation</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5688">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5688">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5690">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5690">Blendable RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5692">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5692">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5693">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5693">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5694">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5694">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5695">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5695">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5696">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5696">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5697">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5697">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5698">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5698">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5699">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5699">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5700">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5700">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5701">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5701">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5702">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5702">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5703">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5703">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5704">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5704">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5705">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5705">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5707">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5707">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5709">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5709">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5711">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5711">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5713">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5713">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5715">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5715">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5717">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5718">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-5719">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5719">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5720">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5720">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5721">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5721">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5722">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5722">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-5723">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5723">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="a2762-5724">DXGI_FORMAT_B8G8R8A8 \_ Typen losen<sup>PCs</sup> (90)</span><span class="sxs-lookup"><span data-stu-id="a2762-5724">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="a2762-5725">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5725">Target</span></span> | <span data-ttu-id="a2762-5726">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5726">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5727">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5727">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5728">32</span><span class="sxs-lookup"><span data-stu-id="a2762-5728">32</span></span> |
| <span data-ttu-id="a2762-5729">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5729">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5731">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5731">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5732">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5732">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5733">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5734">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5735">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5737">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5739">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5741">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5743">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5743">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-5744">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5744">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-5745">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5745">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5746">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5746">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5747">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5747">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5748">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5748">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5749">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5749">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5751">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5751">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-5752">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5752">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5753">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5753">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5754">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5754">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5755">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5755">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5756">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5756">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5757">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5757">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5758">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5758">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5759">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5759">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5760">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5760">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5761">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5761">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5762">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5762">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5763">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5763">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5764">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5764">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5765">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5765">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5766">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5766">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5767">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5767">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5769">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5770">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5771">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-5772">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-5773">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5773">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-5774">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5775">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5775">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5777">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5777">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5778">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5778">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5779">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5779">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5780">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5780">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5782">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="a2762-5783">DXGI_FORMAT_B8G8R8A8 \_ unorm-Datei-<sup>e</sup> /a (87)</span><span class="sxs-lookup"><span data-stu-id="a2762-5783">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="a2762-5784">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5784">Target</span></span> | <span data-ttu-id="a2762-5785">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5785">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5786">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5787">32</span><span class="sxs-lookup"><span data-stu-id="a2762-5787">32</span></span> |
| <span data-ttu-id="a2762-5788">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5788">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5790">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5790">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5792">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5792">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5794">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5794">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5795">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5795">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5796">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5796">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5798">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5798">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5800">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5800">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5802">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5802">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5804">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5804">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5806">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5806">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5808">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5808">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5809">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5809">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5810">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5810">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5811">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5811">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5812">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5812">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5814">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5814">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5816">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5816">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5818">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5818">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5820">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5820">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5821">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5821">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5822">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5822">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5823">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5823">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5824">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5824">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5825">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5825">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5826">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5826">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5827">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5827">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5828">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5828">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5829">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5829">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5830">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5830">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5831">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5831">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5832">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5832">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5833">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5833">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5835">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5835">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5837">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5837">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5839">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5839">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5841">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5841">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5843">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5843">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5845">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5845">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5847">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5847">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5849">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5849">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5850">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5850">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5852">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5852">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5854">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5854">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5856">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5856">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="a2762-5857">DXGI_FORMAT_B8G8R8A8 \_ unorm \_ sRGB-Datei-<sup>e</sup> /a (91)</span><span class="sxs-lookup"><span data-stu-id="a2762-5857">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="a2762-5858">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5858">Target</span></span> | <span data-ttu-id="a2762-5859">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5859">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5860">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5860">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5861">32</span><span class="sxs-lookup"><span data-stu-id="a2762-5861">32</span></span> |
| <span data-ttu-id="a2762-5862">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5862">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5864">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5864">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5865">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5865">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5866">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5866">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5867">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5867">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5868">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5868">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5870">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5872">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5872">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5874">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5874">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5876">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5876">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5878">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5878">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5880">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5880">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5881">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5881">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5882">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5882">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5883">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5883">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5884">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5884">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5886">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5886">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5888">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5888">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5890">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5890">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5892">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5893">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5894">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5895">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5896">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5897">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5898">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5899">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5900">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5901">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5902">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5903">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5904">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5905">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5905">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5907">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5907">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5909">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5909">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5911">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5911">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5913">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5913">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5915">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5915">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5917">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5917">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5919">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5919">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5921">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5921">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5922">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5922">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5924">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5924">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-5926">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5926">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5928">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="a2762-5929">DXGI_FORMAT_B8G8R8X8 \_ Typen losen<sup>PCs</sup> (92)</span><span class="sxs-lookup"><span data-stu-id="a2762-5929">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="a2762-5930">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5930">Target</span></span> | <span data-ttu-id="a2762-5931">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5931">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5932">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5933">32</span><span class="sxs-lookup"><span data-stu-id="a2762-5933">32</span></span> |
| <span data-ttu-id="a2762-5934">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5934">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5936">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5936">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5937">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5937">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5938">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5938">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5939">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5939">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-5940">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-5940">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5942">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-5942">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5944">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-5944">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5946">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-5946">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5948">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-5948">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-5949">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5949">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-5950">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5950">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-5951">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-5951">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-5952">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-5952">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-5953">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-5953">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-5954">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5954">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5956">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-5956">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-5957">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5957">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5958">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5958">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5959">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-5959">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-5960">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5960">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-5961">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5961">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5962">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-5962">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-5963">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-5963">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-5964">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-5964">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-5965">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5965">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-5966">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-5966">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-5967">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-5967">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-5968">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-5968">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-5969">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-5969">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-5970">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-5970">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5971">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-5971">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-5972">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-5972">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5974">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5974">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5975">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-5975">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-5976">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-5976">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-5977">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-5977">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-5978">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-5978">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-5979">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-5979">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-5980">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-5980">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5982">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-5982">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-5983">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5983">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-5984">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-5984">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-5985">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5985">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5987">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-5987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="a2762-5988">DXGI_FORMAT_B8G8R8X8 \_ unorm-Datei-<sup>e</sup> /a (88)</span><span class="sxs-lookup"><span data-stu-id="a2762-5988">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="a2762-5989">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-5989">Target</span></span> | <span data-ttu-id="a2762-5990">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-5990">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-5991">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-5991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-5992">32</span><span class="sxs-lookup"><span data-stu-id="a2762-5992">32</span></span> |
| <span data-ttu-id="a2762-5993">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-5993">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5995">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-5995">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5997">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-5997">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-5999">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-5999">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6000">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6000">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6001">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6001">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6003">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6005">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6007">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6009">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6009">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6011">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6011">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6013">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6013">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6014">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6014">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6015">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6015">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6016">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6016">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6017">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6017">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6019">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6019">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6021">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6021">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6023">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6023">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6025">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6025">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6026">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6026">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6027">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6027">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6028">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6028">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6029">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6029">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6030">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6030">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6031">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6031">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6032">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6032">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6033">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6033">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6034">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6034">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6035">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6035">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6036">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6036">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6037">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6037">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6038">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6038">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6040">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6040">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6042">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6042">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6044">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6044">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6046">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6046">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6048">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6048">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6050">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6050">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6051">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6051">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6053">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6053">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-6054">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6054">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6056">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6056">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6058">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6058">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6060">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6060">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="a2762-6061">DXGI_FORMAT_B8G8R8X8 \_ unorm \_ sRGB-Datei-<sup>e</sup> /a (93)</span><span class="sxs-lookup"><span data-stu-id="a2762-6061">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="a2762-6062">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6062">Target</span></span> | <span data-ttu-id="a2762-6063">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6063">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6064">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6064">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6065">32</span><span class="sxs-lookup"><span data-stu-id="a2762-6065">32</span></span> |
| <span data-ttu-id="a2762-6066">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6066">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6068">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6068">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6069">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6069">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6070">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6070">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6071">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6071">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6072">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6072">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6074">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6074">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6076">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6076">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6078">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6080">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6080">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6082">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6082">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6084">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6084">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6085">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6085">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6086">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6086">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6087">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6087">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6088">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6088">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6090">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6090">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6092">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6092">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6094">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6094">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6096">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6096">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6097">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6097">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6098">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6098">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6099">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6099">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6100">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6100">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6101">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6101">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6102">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6102">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6103">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6103">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6104">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6104">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6105">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6105">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6106">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6106">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6107">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6107">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6108">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6108">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6109">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6109">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6111">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6111">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6113">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6113">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6115">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6115">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6117">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6117">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6119">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6119">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6121">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6121">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6122">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6122">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6124">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6124">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-6125">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6125">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-6126">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6126">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-6127">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6127">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6129">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6129">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="a2762-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="a2762-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="a2762-6131">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6131">Target</span></span> | <span data-ttu-id="a2762-6132">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6132">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6133">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6133">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6134">32</span><span class="sxs-lookup"><span data-stu-id="a2762-6134">32</span></span> |
| <span data-ttu-id="a2762-6135">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6135">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6137">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6137">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6138">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6138">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6139">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6139">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6140">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6140">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6141">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6141">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6142">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6142">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6144">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6144">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6145">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6145">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6146">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6146">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6148">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6148">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6150">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6150">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6151">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6151">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6152">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6152">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6153">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6153">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6154">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6154">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6156">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6156">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6158">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6158">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6160">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6160">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6162">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6162">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6163">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6163">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6164">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6164">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6165">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6165">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6166">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6166">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6167">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6167">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6168">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6168">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6169">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6169">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6170">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6170">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6171">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6171">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6172">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6172">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6173">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6173">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6174">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6174">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6175">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6175">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6177">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6178">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6179">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6180">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6181">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6181">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6182">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6183">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6184">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6184">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6186">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6186">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6188">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6188">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6190">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6190">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6192">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6192">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="a2762-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="a2762-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="a2762-6194">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6194">Target</span></span> | <span data-ttu-id="a2762-6195">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6195">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6196">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6196">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6197">32</span><span class="sxs-lookup"><span data-stu-id="a2762-6197">32</span></span> |
| <span data-ttu-id="a2762-6198">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6198">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6200">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6200">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6201">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6201">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6202">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6202">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6203">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6203">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6204">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6204">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6205">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6205">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6207">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6207">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6208">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6208">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6209">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6209">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6211">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6211">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6213">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6213">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6214">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6214">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6215">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6215">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6216">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6216">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6217">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6217">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6218">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6218">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6219">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6219">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6220">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6220">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6221">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6221">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6222">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6222">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6223">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6223">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6224">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6224">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6225">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6225">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6226">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6226">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6227">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6227">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6228">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6228">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6229">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6229">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6230">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6230">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6231">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6231">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6232">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6232">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6233">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6233">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6234">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6234">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6236">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6236">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6237">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6237">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6238">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6238">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6239">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6239">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6240">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6240">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6241">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6241">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6242">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6242">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6243">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6243">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6245">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6245">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6247">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6247">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6249">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6249">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6251">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="a2762-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="a2762-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="a2762-6253">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6253">Target</span></span> | <span data-ttu-id="a2762-6254">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6254">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6255">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6256">64</span><span class="sxs-lookup"><span data-stu-id="a2762-6256">64</span></span> |
| <span data-ttu-id="a2762-6257">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6257">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6259">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6259">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6260">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6260">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6261">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6261">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6262">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6262">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6263">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6263">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6264">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6264">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6266">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6266">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6267">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6267">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6268">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6268">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6270">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6270">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6272">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6272">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6273">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6273">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6274">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6274">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6275">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6275">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6276">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6276">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6278">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6279">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6279">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6280">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6281">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6282">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6283">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6284">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6285">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6285">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6286">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6287">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6288">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6289">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6291">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6292">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6293">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6294">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6294">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6296">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6297">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6298">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6299">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6300">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6300">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6301">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6302">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6303">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6303">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6305">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6305">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6307">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6307">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6309">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6309">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6311">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="a2762-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="a2762-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="a2762-6313">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6313">Target</span></span> | <span data-ttu-id="a2762-6314">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6314">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6315">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6316">8</span><span class="sxs-lookup"><span data-stu-id="a2762-6316">8</span></span> |
| <span data-ttu-id="a2762-6317">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6317">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6319">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6319">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6320">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6320">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6321">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6321">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6322">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6322">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6323">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6323">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6324">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6324">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6326">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6326">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6327">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6328">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6328">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6330">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6330">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6332">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6332">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6333">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6333">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6334">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6334">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6335">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6335">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6336">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6336">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6337">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6337">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6338">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6338">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6340">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6340">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6342">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6343">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6344">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6345">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6346">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6346">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6347">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6348">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6349">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6350">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6352">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6353">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6354">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6355">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6355">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6357">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6358">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6359">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6360">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6361">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6361">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6362">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6363">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6364">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6364">Video Decoder Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6366">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6366">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6368">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6368">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6370">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6370">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6372">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="a2762-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="a2762-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="a2762-6374">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6374">Target</span></span> | <span data-ttu-id="a2762-6375">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6375">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6376">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6377">16</span><span class="sxs-lookup"><span data-stu-id="a2762-6377">16</span></span> |
| <span data-ttu-id="a2762-6378">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6378">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6380">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6380">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6381">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6381">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6382">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6382">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6383">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6383">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6384">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6384">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6385">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6385">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6387">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6387">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6388">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6388">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6389">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6389">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6391">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6391">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6393">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6393">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6394">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6394">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6395">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6395">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6396">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6396">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6397">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6397">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6398">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6399">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6399">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6401">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6401">Blendable RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6403">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6403">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6404">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6404">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6405">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6405">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6406">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6406">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6407">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6407">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6408">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6408">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6409">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6409">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6410">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6410">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6411">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6411">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6412">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6412">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6413">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6413">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6414">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6414">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6415">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6415">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6416">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6416">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6418">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6418">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6419">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6419">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6420">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6420">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6421">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6421">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6422">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6422">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6423">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6423">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6424">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6424">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6425">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6425">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6427">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6427">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6429">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6429">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6431">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6431">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6433">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6433">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="a2762-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="a2762-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="a2762-6435">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6435">Target</span></span> | <span data-ttu-id="a2762-6436">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6436">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6437">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6437">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6438">16</span><span class="sxs-lookup"><span data-stu-id="a2762-6438">16</span></span> |
| <span data-ttu-id="a2762-6439">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6439">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6441">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6441">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6442">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6442">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6443">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6443">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6444">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6444">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6445">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6445">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6446">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6446">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6448">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6448">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6449">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6449">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6450">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6450">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6452">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6452">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6454">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6454">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6455">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6455">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6456">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6456">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6457">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6457">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6458">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6458">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6459">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6460">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6460">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6462">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6462">Blendable RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6464">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6465">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6466">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6467">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6468">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6468">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6469">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6470">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6471">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6472">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6473">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6474">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6475">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6476">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6477">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6477">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6479">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6480">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6481">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6482">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6483">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6483">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6484">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6485">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6486">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6486">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6488">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6488">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6490">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6490">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6492">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6492">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6494">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="a2762-6495">DXGI_FORMAT_420 nicht transparent \_ <sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="a2762-6495">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="a2762-6496">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6496">Target</span></span> | <span data-ttu-id="a2762-6497">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6497">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6498">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6499">8</span><span class="sxs-lookup"><span data-stu-id="a2762-6499">8</span></span> |
| <span data-ttu-id="a2762-6500">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6500">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6502">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6502">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6503">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6503">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6504">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6504">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6505">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6505">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6506">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6506">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6507">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6507">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6509">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6509">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6510">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6510">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6511">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6511">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-6512">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6512">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-6513">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6513">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6514">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6514">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6515">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6515">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6516">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6516">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6517">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6517">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6518">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6518">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6519">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6519">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6520">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6520">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6521">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6521">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6522">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6522">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6523">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6523">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6524">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6524">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6525">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6525">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6526">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6526">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6527">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6527">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6528">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6528">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6529">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6529">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6530">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6530">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6531">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6531">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6532">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6532">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6533">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6533">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6534">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6534">CPU Lockable</span></span> | \- |
| <span data-ttu-id="a2762-6535">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6535">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6536">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6536">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6537">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6537">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6538">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6538">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6539">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6539">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6540">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6540">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6541">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6541">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6542">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6542">Video Decoder Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6544">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6544">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6546">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6546">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6548">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6548">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6550">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="a2762-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="a2762-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="a2762-6552">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6552">Target</span></span> | <span data-ttu-id="a2762-6553">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6553">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6554">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6555">16</span><span class="sxs-lookup"><span data-stu-id="a2762-6555">16</span></span> |
| <span data-ttu-id="a2762-6556">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6556">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6558">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6558">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6559">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6559">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6560">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6560">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6561">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6561">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6562">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6562">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6563">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6563">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6565">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6565">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6566">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6566">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6567">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6567">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6569">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6569">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6571">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6571">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6572">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6572">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6573">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6573">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6574">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6574">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6575">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6575">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6576">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6576">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6577">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6577">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6578">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6578">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6579">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6579">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6580">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6580">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6581">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6581">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6582">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6582">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6583">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6583">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6584">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6584">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6585">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6585">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6586">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6586">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6587">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6587">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6588">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6588">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6589">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6589">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6590">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6590">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6591">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6591">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6592">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6592">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6594">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6594">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6595">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6595">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6596">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6596">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6597">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6597">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6598">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6598">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6599">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6599">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6600">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6600">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6601">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6601">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6603">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6603">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6605">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6605">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6607">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6607">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6609">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6609">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="a2762-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="a2762-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="a2762-6611">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6611">Target</span></span> | <span data-ttu-id="a2762-6612">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6612">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6613">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6613">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6614">32</span><span class="sxs-lookup"><span data-stu-id="a2762-6614">32</span></span> |
| <span data-ttu-id="a2762-6615">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6615">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6617">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6617">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6618">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6618">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6619">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6619">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6620">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6620">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6621">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6621">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6622">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6622">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6624">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6624">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6625">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6625">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6626">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6626">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6628">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6628">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6630">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6630">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6631">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6631">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6632">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6632">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6633">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6633">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6634">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6634">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6635">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6635">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6636">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6636">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6637">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6637">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6638">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6638">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6639">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6639">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6640">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6640">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6641">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6641">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6642">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6642">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6643">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6643">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6644">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6644">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6645">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6645">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6646">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6646">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6647">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6647">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6648">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6648">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6649">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6649">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6650">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6650">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6651">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6651">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6653">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6653">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6654">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6654">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6655">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6655">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6656">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6656">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6657">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6657">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6658">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6658">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6659">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6659">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6660">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6660">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6662">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6662">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6664">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6664">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6666">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6666">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6668">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6668">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="a2762-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="a2762-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="a2762-6670">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6670">Target</span></span> | <span data-ttu-id="a2762-6671">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6671">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6672">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6672">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6673">32</span><span class="sxs-lookup"><span data-stu-id="a2762-6673">32</span></span> |
| <span data-ttu-id="a2762-6674">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6674">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6676">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6676">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6677">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6677">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6678">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6678">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6679">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6679">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6680">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6680">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6681">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6681">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6683">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6683">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6684">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6684">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6685">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6685">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6687">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6687">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6689">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6689">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6690">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6690">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6691">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6691">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6692">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6692">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6693">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6693">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6694">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6694">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6695">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6695">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6696">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6696">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6697">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6697">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6698">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6698">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6699">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6699">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6700">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6700">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6701">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6701">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6702">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6702">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6703">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6703">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6704">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6704">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6705">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6705">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6706">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6706">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6707">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6707">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6708">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6708">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6709">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6709">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6710">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6710">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6712">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6712">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6713">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6713">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6714">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6714">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6715">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6715">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6716">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6716">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6717">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6718">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6719">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6719">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6721">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6721">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6723">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6723">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6725">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6725">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6727">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6727">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="a2762-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="a2762-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="a2762-6729">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6729">Target</span></span> | <span data-ttu-id="a2762-6730">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6730">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6731">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6731">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6732">8</span><span class="sxs-lookup"><span data-stu-id="a2762-6732">8</span></span> |
| <span data-ttu-id="a2762-6733">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6733">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6735">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6735">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6736">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6736">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6737">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6737">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6738">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6738">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6739">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6739">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6740">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6740">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6742">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6742">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6743">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6743">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6744">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6744">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6746">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6746">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6748">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6748">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6749">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6749">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6750">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6750">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6751">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6752">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6752">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6753">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6753">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6754">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6754">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6756">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6756">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6758">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6758">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6759">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6759">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6760">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6760">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6761">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6761">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6762">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6762">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6763">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6763">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6764">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6764">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6765">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6765">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6766">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6766">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6767">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6767">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6768">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6768">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6769">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6769">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6770">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6770">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6771">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6771">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6773">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6773">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6774">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6774">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6775">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6775">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6776">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6776">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6777">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6777">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6778">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6778">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6779">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6779">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6780">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6780">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6782">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6782">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6784">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6784">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6786">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6786">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6788">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6788">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="a2762-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="a2762-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="a2762-6790">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6790">Target</span></span> | <span data-ttu-id="a2762-6791">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6791">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6792">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6792">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6793">8</span><span class="sxs-lookup"><span data-stu-id="a2762-6793">8</span></span> |
| <span data-ttu-id="a2762-6794">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6794">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6796">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6796">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6797">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6797">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6798">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6798">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6799">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6799">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6800">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6800">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6801">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6801">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6803">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6803">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6804">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6804">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6805">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6805">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-6806">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6806">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-6807">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6807">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6808">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6808">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6809">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6809">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6810">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6810">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6811">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6811">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6812">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6812">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6813">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6814">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6814">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6815">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6815">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6816">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6816">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6817">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6817">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6818">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6818">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6819">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6819">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6820">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6820">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6821">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6821">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6822">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6822">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6823">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6823">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6824">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6824">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6825">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6825">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6826">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6826">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6827">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6827">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6828">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6828">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6830">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6830">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6831">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6831">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6832">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6832">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6833">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6834">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6834">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6835">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6836">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6836">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6837">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6837">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-6838">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6838">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6840">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-6841">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6841">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-6842">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6842">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="a2762-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="a2762-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="a2762-6844">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6844">Target</span></span> | <span data-ttu-id="a2762-6845">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6845">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6846">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6846">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6847">8</span><span class="sxs-lookup"><span data-stu-id="a2762-6847">8</span></span> |
| <span data-ttu-id="a2762-6848">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6848">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6850">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6850">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6851">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6851">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6852">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6852">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6853">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6853">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6854">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6854">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6855">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6855">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6857">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6857">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6858">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6859">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6859">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-6860">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6860">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-6861">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6861">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6862">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6862">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6863">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6863">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6864">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6864">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6865">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6865">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6866">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6867">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6867">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6868">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6869">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6870">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6871">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6872">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6873">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6873">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6874">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6875">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6876">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6877">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6878">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6879">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6880">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6881">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6882">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6882">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6884">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6885">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6886">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6887">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6888">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6888">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6889">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6890">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6890">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6891">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6891">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-6892">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6892">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6894">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-6895">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6895">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-6896">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6896">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="a2762-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="a2762-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="a2762-6898">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6898">Target</span></span> | <span data-ttu-id="a2762-6899">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6899">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6900">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6900">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6901">8</span><span class="sxs-lookup"><span data-stu-id="a2762-6901">8</span></span> |
| <span data-ttu-id="a2762-6902">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6902">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6904">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6904">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6905">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6905">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6906">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6906">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6907">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6907">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6908">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6908">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6909">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6909">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6911">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6911">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6912">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6912">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6913">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6913">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-6914">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6914">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-6915">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6915">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6916">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6916">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6917">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6917">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6918">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6918">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6919">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6919">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6920">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6920">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6921">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6921">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6922">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6922">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6923">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6923">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6924">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6924">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6925">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6925">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6926">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6926">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6927">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6927">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6928">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6928">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6929">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6929">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6930">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6930">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6931">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6931">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6932">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6932">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6933">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6933">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6934">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6934">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6935">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6935">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6936">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6936">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6938">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6938">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6939">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6939">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6940">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6940">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6941">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6941">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6942">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6942">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6943">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6943">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6944">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6944">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6945">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6945">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-6946">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6946">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6948">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-6948">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-6949">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6949">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-6950">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-6950">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="a2762-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="a2762-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="a2762-6952">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6952">Target</span></span> | <span data-ttu-id="a2762-6953">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-6953">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-6954">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-6954">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-6955">16</span><span class="sxs-lookup"><span data-stu-id="a2762-6955">16</span></span> |
| <span data-ttu-id="a2762-6956">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-6956">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-6958">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6958">Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6959">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-6959">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6960">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-6960">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6961">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-6961">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-6962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-6962">Texture1D</span></span> | \- |
| <span data-ttu-id="a2762-6963">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-6963">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6965">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-6965">Texture3D</span></span> | \- |
| <span data-ttu-id="a2762-6966">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-6966">TextureCube</span></span> | \- |
| <span data-ttu-id="a2762-6967">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-6967">Shader ld</span></span> | \- |
| <span data-ttu-id="a2762-6968">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6968">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a2762-6969">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6969">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-6970">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-6970">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-6971">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-6971">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-6972">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-6972">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-6973">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6973">Mipmap</span></span> | \- |
| <span data-ttu-id="a2762-6974">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-6974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a2762-6975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6975">RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6976">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6977">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-6977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-6978">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-6978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-6979">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6980">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-6980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-6981">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-6981">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-6982">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-6982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-6983">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-6984">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-6984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-6985">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-6985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-6986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-6986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-6987">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-6987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-6988">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-6988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6989">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-6989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-6990">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-6990">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-6992">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6993">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-6993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a2762-6994">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-6994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a2762-6995">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-6995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a2762-6996">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-6996">Multisample Load</span></span> | \- |
| <span data-ttu-id="a2762-6997">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-6997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-6998">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-6998">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-6999">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-6999">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-7000">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-7000">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-7002">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-7002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-7003">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-7003">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-7004">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-7004">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="a2762-7005">DXGI_FORMAT_B4G4R4A4 \_ unorm<sup></sup> -Fehler (115)</span><span class="sxs-lookup"><span data-stu-id="a2762-7005">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="a2762-7006">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-7006">Target</span></span> | <span data-ttu-id="a2762-7007">Support</span><span class="sxs-lookup"><span data-stu-id="a2762-7007">Support</span></span> |
| - | - |
| <span data-ttu-id="a2762-7008">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="a2762-7008">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a2762-7009">16</span><span class="sxs-lookup"><span data-stu-id="a2762-7009">16</span></span> |
| <span data-ttu-id="a2762-7010">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a2762-7010">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-7012">Buffer</span><span class="sxs-lookup"><span data-stu-id="a2762-7012">Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-7014">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="a2762-7014">Input Assembler Vertex Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-7016">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="a2762-7016">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a2762-7017">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="a2762-7017">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a2762-7018">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a2762-7018">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-7020">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a2762-7020">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-7022">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a2762-7022">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-7024">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a2762-7024">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-7026">Shader LD</span><span class="sxs-lookup"><span data-stu-id="a2762-7026">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-7028">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-7028">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-7030">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-7030">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a2762-7031">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="a2762-7031">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a2762-7032">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="a2762-7032">Shader gather4</span></span> | \- |
| <span data-ttu-id="a2762-7033">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a2762-7033">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a2762-7034">MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-7034">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-7036">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="a2762-7036">Mipmap Auto-Generation</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-7038">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-7038">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-7040">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-7040">Blendable RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-7042">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="a2762-7042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a2762-7043">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="a2762-7043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a2762-7044">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-7044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-7045">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="a2762-7045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a2762-7046">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="a2762-7046">Typed UAV</span></span> | \- |
| <span data-ttu-id="a2762-7047">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="a2762-7047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a2762-7048">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-7048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a2762-7049">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="a2762-7049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a2762-7050">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="a2762-7050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a2762-7051">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a2762-7051">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a2762-7052">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="a2762-7052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a2762-7053">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="a2762-7053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-7054">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="a2762-7054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a2762-7055">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="a2762-7055">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-7057">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-7057">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-7059">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="a2762-7059">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-7061">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="a2762-7061">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-7063">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="a2762-7063">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="a2762-7065">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="a2762-7065">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="a2762-7067">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a2762-7067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a2762-7068">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="a2762-7068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a2762-7069">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="a2762-7069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a2762-7070">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-7070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a2762-7071">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="a2762-7071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a2762-7072">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-7072">Shared Resource</span></span> | \- |
| <span data-ttu-id="a2762-7073">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="a2762-7073">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="a2762-7074">Notizen formatieren</span><span class="sxs-lookup"><span data-stu-id="a2762-7074">Format notes</span></span>

<span data-ttu-id="a2762-7075">Der Zweck des-Formats kann sich von einer Hardware Funktionsebene zur nächsten ändern.</span><span class="sxs-lookup"><span data-stu-id="a2762-7075">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="a2762-7076"><sup>L</sup> : typloses Format</span><span class="sxs-lookup"><span data-stu-id="a2762-7076"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="a2762-7077"><sup>PCs</sup> : teilweise typisiertes, castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="a2762-7077"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="a2762-7078"><sup>FCS</sup> : vollständig typisiertes, castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="a2762-7078"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="a2762-7079"><sup>FNS</sup> : vollständig typisiertes, nicht-castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="a2762-7079"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="a2762-7080"><sup>PCC</sup> : teilweise typisiertes, castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="a2762-7080"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="a2762-7081"><sup>FCC</sup> : vollständig typisiertes, castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="a2762-7081"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="a2762-7082"><sup>FNC</sup> : vollständig typisiertes, nicht-castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="a2762-7082"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="a2762-7083"><sup>V</sup> : Videoformat</span><span class="sxs-lookup"><span data-stu-id="a2762-7083"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="a2762-7084">Backpuffer und Scanvorgänge im [**DXGI- \_ Format \_ R16G16B16A16 \_ float**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Format enthalten lineare Gamma-Daten.</span><span class="sxs-lookup"><span data-stu-id="a2762-7084">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2762-7085">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a2762-7085">Related topics</span></span>

[<span data-ttu-id="a2762-7086">D3D12-Hardware Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="a2762-7086">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="a2762-7087">**ID3D10Device:: checkformatsupport**</span><span class="sxs-lookup"><span data-stu-id="a2762-7087">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="a2762-7088">Programmier Handbuch für DXGI</span><span class="sxs-lookup"><span data-stu-id="a2762-7088">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
