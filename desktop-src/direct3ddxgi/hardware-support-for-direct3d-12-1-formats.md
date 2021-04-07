---
description: In diesem Abschnitt werden die Formate ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die auf Direct3D Feature Level 12,1-Hardware unterstützt werden.
ms.assetid: 0DC50FF3-3193-4F3B-9976-EE504C6FCC87
title: Formatunterstützung für Direct3D 12.1-Hardware auf Featureebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d20b00a2cfb5b0343a2ebb1a56a1253ddd1966
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745376"
---
# <a name="format-support-for-direct3d-feature-level-121-hardware"></a><span data-ttu-id="937fc-103">Formatunterstützung für Direct3D 12.1-Hardware auf Featureebene</span><span class="sxs-lookup"><span data-stu-id="937fc-103">Format support for Direct3D Feature Level 12.1 hardware</span></span>

<span data-ttu-id="937fc-104">In diesem Abschnitt werden die Formate ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die auf Direct3D Feature Level 12,1-Hardware unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="937fc-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 12.1 hardware.</span></span>

<span data-ttu-id="937fc-105">Die Tabelle enthält eine Zusammenfassung der Featureunterstützung, die den folgenden Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="937fc-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="937fc-106">Symbol</span><span class="sxs-lookup"><span data-stu-id="937fc-106">Symbol</span></span>                            | <span data-ttu-id="937fc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="937fc-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="937fc-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="937fc-108">_ *-*\*</span></span>                             | <span data-ttu-id="937fc-109">Nicht zulässig oder nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="937fc-109">Disallowed or not available.</span></span>                                                  |
| ![Erforderlich](images/letter-r.jpg)  | <span data-ttu-id="937fc-111">Hardware Unterstützung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="937fc-111">Hardware support is required.</span></span>                                                 |
| ![Optional](images/letter-o.jpg)  | <span data-ttu-id="937fc-113">Hardwareunterstützung optional, das Format ist möglicherweise Hardware beschleunigt.</span><span class="sxs-lookup"><span data-stu-id="937fc-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![lässe](images/letter-d.jpg) | <span data-ttu-id="937fc-115">Erforderlich, wenn eine zugehörige optionale Funktion unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="937fc-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="937fc-116">Dieses Thema enthält einen Abschnitt Pro Format.</span><span class="sxs-lookup"><span data-stu-id="937fc-116">This topic contains a section per format.</span></span> <span data-ttu-id="937fc-117">Ein Format *Ziel* (die Tabellen enthalten eine Zeile pro Ziel) kann ein Ressourcentyp, eine intrinsische HLSL-Funktion oder eine bestimmte Funktionalität sein, die von einem bestimmten Format abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="937fc-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="937fc-118">Informationen zur programmgesteuerten Überprüfung der Formatunterstützung in D3D11 und D3D12 finden Sie unter über [Prüfen der Unterstützung von Hardwarefunktionen](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="937fc-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="937fc-119">Die Zahlen der Formate sind größtenteils, aber nicht alle in aufsteigender numerischer Reihenfolge, dass einige nicht in &mdash; numerischer Reihenfolge sind und neben anderen relevanten Formaten aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="937fc-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="937fc-120">Beachten Sie auch, dass *typlose* in einem Format Namen *teilweise* typisiert und nicht streng typlos sein kann (Weitere Informationen finden Sie im Abschnitt " [Format Notizen](#format-notes) " am Ende des Themas).</span><span class="sxs-lookup"><span data-stu-id="937fc-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="937fc-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="937fc-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="937fc-122">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-122">Target</span></span> | <span data-ttu-id="937fc-123">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-123">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-124">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-125">0</span><span class="sxs-lookup"><span data-stu-id="937fc-125">0</span></span> |
| <span data-ttu-id="937fc-126">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-126">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-128">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-130">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-131">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-132">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-133">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-134">Texture2D</span></span> | \- |
| <span data-ttu-id="937fc-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-135">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-136">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-137">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-137">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-138">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-139">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-139">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-140">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-140">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-141">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-142">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-142">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-143">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-143">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-144">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-144">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-146">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-147">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-148">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-149">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-150">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-150">Structured UAV and SRV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-152">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-152">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-153">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-153">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-154">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-154">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-155">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-155">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-156">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-156">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-157">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-157">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-158">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-158">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-159">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-159">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-160">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-160">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-161">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-161">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-163">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-163">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-164">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-164">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-165">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-165">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-166">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-166">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-167">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-167">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-168">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-168">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-169">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-169">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-170">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-170">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-171">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-171">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-172">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-172">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-173">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-173">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-174">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-174">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-175">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-175">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="937fc-177">DXGI_FORMAT_R32G32B32A32_TYPELESS<sup>PCs</sup> (1)</span><span class="sxs-lookup"><span data-stu-id="937fc-177">DXGI_FORMAT_R32G32B32A32_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="937fc-178">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-178">Target</span></span> | <span data-ttu-id="937fc-179">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-179">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-180">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-180">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-181">128</span><span class="sxs-lookup"><span data-stu-id="937fc-181">128</span></span> |
| <span data-ttu-id="937fc-182">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-182">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-184">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-184">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-185">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-185">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-186">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-186">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-187">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-187">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-188">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-188">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-190">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-190">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-192">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-192">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-194">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-194">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-196">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-196">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-197">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-197">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-198">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-198">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-199">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-199">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-200">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-200">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-201">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-201">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-202">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-202">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-204">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-204">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-205">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-205">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-206">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-206">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-207">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-207">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-208">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-208">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-209">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-209">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-210">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-210">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-211">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-211">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-212">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-212">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-213">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-213">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-214">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-215">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-216">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-216">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-217">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-218">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-218">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-219">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-219">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-220">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-220">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-222">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-223">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-224">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-225">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-226">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-226">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-227">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-228">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-228">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-230">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-230">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-231">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-231">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-232">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-232">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-233">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-233">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-235">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-235">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-236">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-236">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="937fc-238">DXGI_FORMAT_R32G32B32A32_FLOAT<sup>-</sup> Druckkarte (2)</span><span class="sxs-lookup"><span data-stu-id="937fc-238">DXGI_FORMAT_R32G32B32A32_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="937fc-239">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-239">Target</span></span> | <span data-ttu-id="937fc-240">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-240">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-241">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-241">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-242">128</span><span class="sxs-lookup"><span data-stu-id="937fc-242">128</span></span> |
| <span data-ttu-id="937fc-243">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-243">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-245">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-245">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-247">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-247">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-249">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-249">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-250">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-250">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-252">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-252">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-254">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-256">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-256">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-258">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-258">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-260">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-260">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-262">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-262">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-264">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-264">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-265">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-265">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-266">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-266">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-268">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-268">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-269">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-269">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-271">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-271">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-273">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-273">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-275">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-275">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-277">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-277">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-278">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-278">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-279">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-279">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-280">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-280">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-281">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-281">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-283">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-283">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-285">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-285">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-287">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-287">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-288">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-288">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-289">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-289">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-290">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-290">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-291">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-291">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-292">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-292">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-293">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-293">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-295">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-295">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-297">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-297">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-299">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-299">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-301">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-301">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-303">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-303">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-305">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-305">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-306">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-306">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-308">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-308">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-309">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-309">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-310">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-310">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-311">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-311">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-313">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-313">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-314">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-314">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="937fc-316">DXGI_FORMAT_R32G32B32A32_UINT<sup>(</sup> 3)</span><span class="sxs-lookup"><span data-stu-id="937fc-316">DXGI_FORMAT_R32G32B32A32_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="937fc-317">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-317">Target</span></span> | <span data-ttu-id="937fc-318">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-318">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-319">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-320">128</span><span class="sxs-lookup"><span data-stu-id="937fc-320">128</span></span> |
| <span data-ttu-id="937fc-321">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-321">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-323">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-323">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-325">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-325">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-327">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-327">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-328">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-328">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-330">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-330">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-332">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-332">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-334">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-334">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-336">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-338">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-338">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-340">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-340">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-341">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-341">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-342">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-342">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-343">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-343">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-344">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-344">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-345">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-345">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-347">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-347">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-348">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-348">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-350">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-350">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-351">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-351">Output Merger Logic Op</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-353">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-353">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-354">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-354">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-355">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-355">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-356">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-356">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-358">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-358">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-360">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-360">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-362">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-362">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-363">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-363">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-364">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-364">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-365">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-365">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-366">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-366">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-367">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-367">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-368">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-368">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-370">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-370">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-372">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-372">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-374">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-374">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-376">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-376">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-377">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-377">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-379">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-380">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-380">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-382">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-382">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-383">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-383">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-384">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-384">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-385">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-385">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-387">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-387">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-388">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-388">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="937fc-390">DXGI_FORMAT_R32G32B32A32_SINT<sup>(</sup> 4)</span><span class="sxs-lookup"><span data-stu-id="937fc-390">DXGI_FORMAT_R32G32B32A32_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="937fc-391">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-391">Target</span></span> | <span data-ttu-id="937fc-392">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-392">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-393">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-394">128</span><span class="sxs-lookup"><span data-stu-id="937fc-394">128</span></span> |
| <span data-ttu-id="937fc-395">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-395">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-397">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-397">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-399">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-399">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-401">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-402">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-402">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-404">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-404">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-406">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-406">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-408">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-408">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-410">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-410">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-412">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-412">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-414">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-414">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-415">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-415">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-416">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-416">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-417">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-417">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-418">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-418">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-419">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-419">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-421">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-421">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-422">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-424">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-424">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-425">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-425">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-426">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-426">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-427">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-427">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-428">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-428">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-429">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-429">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-431">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-431">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-433">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-433">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-435">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-435">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-436">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-436">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-437">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-437">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-438">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-438">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-439">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-439">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-440">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-440">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-441">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-441">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-443">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-443">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-445">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-445">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-447">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-447">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-449">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-449">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-450">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-450">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-452">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-452">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-453">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-453">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-455">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-455">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-456">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-456">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-457">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-457">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-458">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-458">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-460">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-460">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-461">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-461">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="937fc-463">DXGI_FORMAT_R32G32B32_TYPELESS<sup>PCs</sup> (5)</span><span class="sxs-lookup"><span data-stu-id="937fc-463">DXGI_FORMAT_R32G32B32_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="937fc-464">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-464">Target</span></span> | <span data-ttu-id="937fc-465">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-465">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-466">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-466">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-467">96</span><span class="sxs-lookup"><span data-stu-id="937fc-467">96</span></span> |
| <span data-ttu-id="937fc-468">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-468">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-470">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-470">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-471">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-471">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-472">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-472">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-473">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-473">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-474">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-474">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-476">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-476">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-478">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-478">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-480">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-480">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-482">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-482">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-483">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-483">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-484">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-484">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-485">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-485">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-486">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-486">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-487">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-487">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-488">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-488">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-490">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-490">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-491">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-491">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-492">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-492">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-493">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-493">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-494">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-494">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-495">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-495">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-496">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-496">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-497">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-497">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-498">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-498">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-499">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-499">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-500">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-500">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-501">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-501">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-502">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-502">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-503">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-503">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-504">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-504">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-505">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-505">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-506">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-506">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-508">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-508">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-509">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-509">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-510">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-510">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-511">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-511">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-512">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-512">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-513">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-513">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-514">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-514">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-516">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-516">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-517">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-517">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-518">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-518">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-519">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-519">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-520">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-520">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-521">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-521">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="937fc-522">DXGI_FORMAT_R32G32B32_FLOAT<sup>(</sup> 6)</span><span class="sxs-lookup"><span data-stu-id="937fc-522">DXGI_FORMAT_R32G32B32_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="937fc-523">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-523">Target</span></span> | <span data-ttu-id="937fc-524">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-524">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-525">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-525">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-526">96</span><span class="sxs-lookup"><span data-stu-id="937fc-526">96</span></span> |
| <span data-ttu-id="937fc-527">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-527">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-529">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-529">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-531">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-531">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-533">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-533">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-534">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-534">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-536">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-536">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-538">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-538">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-540">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-540">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-542">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-542">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-544">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-544">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-546">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-546">Shader sample (any filter)</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-548">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-548">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-549">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-549">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-550">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-550">Shader gather4</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-552">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-552">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-553">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-553">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-555">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-555">Mipmap Auto- Generation</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-557">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-557">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-559">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-559">Blendable RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="937fc-561">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-561">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-562">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-562">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-563">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-563">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-564">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-564">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-565">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-565">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-566">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-566">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-567">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-567">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-568">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-568">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-569">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-569">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-570">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-570">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-571">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-571">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-572">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-572">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-573">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-573">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-574">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-574">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-576">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-576">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="937fc-578">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-578">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="937fc-580">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-580">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-582">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-582">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-584">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-584">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-586">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-586">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-587">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-587">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-589">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-590">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-591">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-592">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-592">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-593">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-593">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-594">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="937fc-595">DXGI_FORMAT_R32G32B32_UINT<sup>(</sup> 7)</span><span class="sxs-lookup"><span data-stu-id="937fc-595">DXGI_FORMAT_R32G32B32_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="937fc-596">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-596">Target</span></span> | <span data-ttu-id="937fc-597">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-597">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-598">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-599">96</span><span class="sxs-lookup"><span data-stu-id="937fc-599">96</span></span> |
| <span data-ttu-id="937fc-600">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-600">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-602">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-602">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-604">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-604">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-606">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-606">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-607">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-607">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-609">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-609">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-611">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-611">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-613">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-613">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-615">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-615">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-617">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-617">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-619">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-620">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-620">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-621">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-621">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-622">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-622">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-623">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-623">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-624">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-624">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-626">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-626">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-627">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-627">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-629">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-629">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-630">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-630">Output Merger Logic Op</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-632">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-632">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-633">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-633">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-634">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-634">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-635">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-635">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-636">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-636">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-637">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-637">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-638">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-638">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-639">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-639">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-640">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-640">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-641">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-641">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-642">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-642">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-643">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-643">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-644">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-644">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-646">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-646">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="937fc-648">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-648">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="937fc-650">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-650">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-652">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-653">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-653">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-655">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-655">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-656">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-656">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-658">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-658">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-659">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-659">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-660">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-660">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-661">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-661">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-662">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-662">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-663">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="937fc-664">DXGI_FORMAT_R32G32B32_SINT-<sup>f</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="937fc-664">DXGI_FORMAT_R32G32B32_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="937fc-665">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-665">Target</span></span> | <span data-ttu-id="937fc-666">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-666">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-667">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-668">96</span><span class="sxs-lookup"><span data-stu-id="937fc-668">96</span></span> |
| <span data-ttu-id="937fc-669">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-669">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-671">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-671">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-673">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-673">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-675">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-675">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-676">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-676">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-678">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-678">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-680">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-680">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-682">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-682">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-684">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-684">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-686">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-686">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-688">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-688">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-689">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-689">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-690">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-690">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-691">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-691">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-692">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-692">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-693">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-693">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-695">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-695">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-696">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-696">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-698">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-698">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-699">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-699">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-700">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-700">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-701">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-701">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-702">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-702">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-703">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-703">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-704">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-704">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-705">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-705">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-706">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-706">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-707">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-707">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-708">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-708">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-709">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-709">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-710">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-710">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-711">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-711">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-712">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-712">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-714">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-714">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="937fc-716">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-716">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="937fc-718">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-718">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-720">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-720">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-721">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-721">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-723">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-723">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-724">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-724">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-726">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-726">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-727">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-727">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-728">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-728">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-729">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-729">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-730">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-730">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-731">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-731">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="937fc-732">DXGI_FORMAT_R16G16B16A16_TYPELESS<sup>PCs</sup> (9)</span><span class="sxs-lookup"><span data-stu-id="937fc-732">DXGI_FORMAT_R16G16B16A16_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="937fc-733">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-733">Target</span></span> | <span data-ttu-id="937fc-734">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-734">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-735">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-735">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-736">64</span><span class="sxs-lookup"><span data-stu-id="937fc-736">64</span></span> |
| <span data-ttu-id="937fc-737">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-737">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-739">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-739">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-740">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-741">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-742">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-743">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-745">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-745">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-747">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-747">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-749">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-749">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-751">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-751">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-752">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-752">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-753">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-753">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-754">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-754">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-755">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-755">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-756">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-756">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-757">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-757">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-759">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-759">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-760">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-760">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-761">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-761">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-762">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-762">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-763">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-763">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-764">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-764">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-765">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-765">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-766">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-766">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-767">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-767">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-768">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-768">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-769">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-769">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-770">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-770">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-771">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-771">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-772">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-772">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-773">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-773">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-774">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-774">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-775">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-775">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-777">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-777">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-778">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-778">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-779">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-779">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-780">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-780">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-781">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-781">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-782">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-782">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-783">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-783">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-785">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-785">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-786">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-786">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-787">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-787">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-788">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-788">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-790">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-790">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-791">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-791">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="937fc-793">DXGI_FORMAT_R16G16B16A16_FLOAT-<sup>f</sup> -(10)</span><span class="sxs-lookup"><span data-stu-id="937fc-793">DXGI_FORMAT_R16G16B16A16_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="937fc-794">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-794">Target</span></span> | <span data-ttu-id="937fc-795">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-795">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-796">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-796">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-797">64</span><span class="sxs-lookup"><span data-stu-id="937fc-797">64</span></span> |
| <span data-ttu-id="937fc-798">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-798">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-800">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-800">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-802">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-802">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-804">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-805">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-806">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-808">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-808">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-810">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-810">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-812">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-812">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-814">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-814">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-816">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-816">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-818">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-818">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-819">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-819">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-820">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-820">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-822">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-822">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-823">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-823">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-825">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-825">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-827">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-827">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-829">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-829">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-831">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-832">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-833">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-834">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-835">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-835">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-837">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-837">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-839">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-839">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-841">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-841">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-842">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-842">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-843">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-843">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-844">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-844">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-845">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-845">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-846">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-846">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-847">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-847">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-849">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-849">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-851">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-851">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-853">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-853">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-855">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-855">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-857">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-857">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-859">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-859">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-861">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-861">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-863">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-864">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-864">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-866">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-866">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-868">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-868">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-870">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-870">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-871">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-871">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="937fc-873">DXGI_FORMAT_R16G16B16A16_UNORM<sup>(</sup> 11)</span><span class="sxs-lookup"><span data-stu-id="937fc-873">DXGI_FORMAT_R16G16B16A16_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="937fc-874">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-874">Target</span></span> | <span data-ttu-id="937fc-875">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-875">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-876">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-876">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-877">64</span><span class="sxs-lookup"><span data-stu-id="937fc-877">64</span></span> |
| <span data-ttu-id="937fc-878">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-878">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-880">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-880">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-882">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-882">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-884">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-884">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-885">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-885">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-886">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-886">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-888">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-888">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-890">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-890">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-892">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-894">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-894">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-896">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-896">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-898">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-898">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-899">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-899">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-900">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-900">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-902">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-902">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-903">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-903">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-905">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-905">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-907">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-909">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-909">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-911">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-912">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-913">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-914">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-915">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-915">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-917">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-917">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-919">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-919">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-921">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-921">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-922">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-922">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-923">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-923">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-924">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-924">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-925">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-925">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-926">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-926">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-927">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-927">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-929">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-929">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-931">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-931">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-933">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-933">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-935">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-935">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-937">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-937">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-939">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-939">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-940">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-940">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-942">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-943">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-944">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-945">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-945">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-947">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-947">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-948">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-948">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="937fc-950">DXGI_FORMAT_R16G16B16A16_UINT<sup>(</sup> 12)</span><span class="sxs-lookup"><span data-stu-id="937fc-950">DXGI_FORMAT_R16G16B16A16_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="937fc-951">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-951">Target</span></span> | <span data-ttu-id="937fc-952">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-952">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-953">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-953">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-954">64</span><span class="sxs-lookup"><span data-stu-id="937fc-954">64</span></span> |
| <span data-ttu-id="937fc-955">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-955">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-957">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-957">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-959">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-959">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-961">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-961">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-962">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-962">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-963">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-963">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-965">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-965">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-967">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-967">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-969">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-969">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-971">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-971">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-973">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-973">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-974">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-974">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-975">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-975">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-976">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-976">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-977">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-977">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-978">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-978">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-980">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-980">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-981">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-981">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-983">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-983">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-984">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-984">Output Merger Logic Op</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-986">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-986">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-987">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-987">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-988">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-988">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-989">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-989">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-991">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-991">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-993">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-993">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-995">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-995">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-996">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-996">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-997">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-997">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-998">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-998">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-999">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-999">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1000">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1000">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1001">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1001">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1003">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1003">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1005">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1005">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1007">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1007">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1009">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-1010">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1010">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1012">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1012">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1013">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1013">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1015">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1015">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1016">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1016">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1017">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1017">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1018">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1018">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1020">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1020">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1021">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1021">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="937fc-1023">DXGI_FORMAT_R16G16B16A16_SNORM<sup>(</sup> 13)</span><span class="sxs-lookup"><span data-stu-id="937fc-1023">DXGI_FORMAT_R16G16B16A16_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="937fc-1024">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1024">Target</span></span> | <span data-ttu-id="937fc-1025">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1025">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1026">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1026">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1027">64</span><span class="sxs-lookup"><span data-stu-id="937fc-1027">64</span></span> |
| <span data-ttu-id="937fc-1028">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1028">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1030">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1030">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1032">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1032">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1034">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1034">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1035">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1035">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1036">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1036">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1038">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1038">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1040">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1040">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1042">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1042">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1044">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1044">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1046">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1046">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1048">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1048">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1049">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1049">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1050">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1050">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1052">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1052">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1053">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1053">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1055">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1055">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1057">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1057">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1059">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1059">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1061">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1061">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-1062">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1062">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1063">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1063">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1064">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1064">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1065">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1065">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1067">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1067">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1069">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1069">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1071">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1071">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1072">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1072">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1073">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1073">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1074">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1074">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1075">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1075">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1076">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1076">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1077">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1077">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1079">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1079">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1081">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1081">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1083">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1083">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1085">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1085">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1087">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1087">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1089">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1089">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1090">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1090">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1092">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1092">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1093">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1093">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1094">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1094">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1095">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1095">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1097">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1097">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1098">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1098">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="937fc-1100">DXGI_FORMAT_R16G16B16A16_SINT<sup>(</sup> (14))</span><span class="sxs-lookup"><span data-stu-id="937fc-1100">DXGI_FORMAT_R16G16B16A16_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="937fc-1101">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1101">Target</span></span> | <span data-ttu-id="937fc-1102">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1102">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1103">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1103">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1104">64</span><span class="sxs-lookup"><span data-stu-id="937fc-1104">64</span></span> |
| <span data-ttu-id="937fc-1105">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1105">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1107">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1107">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1109">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1109">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1111">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1111">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1112">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1112">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1113">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1113">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1115">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1115">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1117">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1117">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1119">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1119">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1121">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1121">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1123">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1123">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-1124">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1124">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1125">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1125">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1126">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1126">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-1127">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1127">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1128">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1128">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1130">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1130">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-1131">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1131">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1133">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1133">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1134">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1134">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-1135">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1135">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1136">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1136">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1137">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1137">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1138">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1138">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1140">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1140">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1142">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1142">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1144">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1144">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1145">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1145">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1146">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1146">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1147">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1147">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1148">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1148">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1149">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1149">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1150">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1150">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1152">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1152">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1154">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1154">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1156">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1156">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1158">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1158">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-1159">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1159">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1161">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1161">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1162">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1162">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1164">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1164">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1165">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1165">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1166">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1166">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1167">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1167">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1169">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1169">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1170">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1170">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="937fc-1172">DXGI_FORMAT_R32G32_TYPELESS<sup>PCs</sup> (15)</span><span class="sxs-lookup"><span data-stu-id="937fc-1172">DXGI_FORMAT_R32G32_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="937fc-1173">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1173">Target</span></span> | <span data-ttu-id="937fc-1174">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1174">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1175">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1175">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1176">64</span><span class="sxs-lookup"><span data-stu-id="937fc-1176">64</span></span> |
| <span data-ttu-id="937fc-1177">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1177">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1179">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1179">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1180">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1180">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1181">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1181">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1182">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1182">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1183">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1183">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1185">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1185">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1187">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1187">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1189">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1191">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1191">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-1192">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1192">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-1193">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1193">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1194">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1194">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1195">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1195">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-1196">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1196">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1197">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1197">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1199">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1199">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-1200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1200">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1201">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1201">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1202">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1202">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-1203">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1203">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1204">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1204">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1205">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1205">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1206">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1206">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-1207">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1207">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-1208">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1208">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-1209">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1209">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1210">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1210">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1211">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1211">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1212">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1212">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1213">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1213">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1214">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1214">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1215">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1215">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1217">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1217">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1218">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1218">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1219">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1219">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-1220">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1220">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-1221">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1221">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-1222">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1222">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1223">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1223">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1225">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1225">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1226">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1226">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1227">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1227">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1228">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1228">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-1229">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1229">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1230">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1230">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="937fc-1232">DXGI_FORMAT_R32G32_FLOAT-<sup>f</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="937fc-1232">DXGI_FORMAT_R32G32_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="937fc-1233">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1233">Target</span></span> | <span data-ttu-id="937fc-1234">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1234">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1235">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1235">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1236">64</span><span class="sxs-lookup"><span data-stu-id="937fc-1236">64</span></span> |
| <span data-ttu-id="937fc-1237">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1237">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1239">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1239">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1241">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1241">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1243">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1243">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1244">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1244">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1246">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1246">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1248">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1248">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1250">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1250">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1252">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1254">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1254">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1256">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1256">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1258">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1258">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1259">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1259">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1260">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1260">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1262">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1262">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1263">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1263">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1265">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1265">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1267">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1269">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1269">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1271">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-1272">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1273">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1274">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1275">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1275">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1277">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1277">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1279">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1279">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1281">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1281">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1282">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1282">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1283">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1283">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1284">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1284">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1285">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1285">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1286">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1286">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1287">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1287">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1289">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1289">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1291">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1291">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1293">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1293">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1295">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1295">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1297">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1297">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1299">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1299">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1300">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1300">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1302">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1302">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1303">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1303">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1304">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1304">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1305">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1305">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-1306">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1306">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1307">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1307">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="937fc-1309">DXGI_FORMAT_R32G32_UINT<sup>(</sup> 17)</span><span class="sxs-lookup"><span data-stu-id="937fc-1309">DXGI_FORMAT_R32G32_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="937fc-1310">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1310">Target</span></span> | <span data-ttu-id="937fc-1311">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1311">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1312">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1312">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1313">64</span><span class="sxs-lookup"><span data-stu-id="937fc-1313">64</span></span> |
| <span data-ttu-id="937fc-1314">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1314">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1316">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1316">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1318">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1318">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1320">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1321">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1321">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1323">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1323">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1325">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1325">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1327">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1327">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1329">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1329">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1331">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1331">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1333">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-1334">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1334">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1335">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1335">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1336">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1336">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-1337">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1337">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1338">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1338">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1340">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1340">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-1341">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1341">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1343">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1343">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1344">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1344">Output Merger Logic Op</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1346">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1346">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1347">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1347">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1348">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1348">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1349">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1349">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1351">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1351">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1353">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1353">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1355">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1355">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1356">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1356">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1357">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1357">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1358">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1358">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1359">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1359">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1360">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1360">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1361">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1361">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1363">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1363">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1365">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1365">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1367">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1367">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1369">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-1370">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1370">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1372">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1373">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1373">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1375">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1375">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1376">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1376">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1377">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1377">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1378">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1378">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-1379">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1379">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1380">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1380">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="937fc-1382">DXGI_FORMAT_R32G32_SINT<sup>(</sup> 18)</span><span class="sxs-lookup"><span data-stu-id="937fc-1382">DXGI_FORMAT_R32G32_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="937fc-1383">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1383">Target</span></span> | <span data-ttu-id="937fc-1384">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1384">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1385">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1385">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1386">64</span><span class="sxs-lookup"><span data-stu-id="937fc-1386">64</span></span> |
| <span data-ttu-id="937fc-1387">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1387">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1389">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1389">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1391">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1391">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1393">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1393">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1394">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1394">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1396">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1396">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1398">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1400">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1400">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1402">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1402">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1404">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1404">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1406">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1406">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-1407">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1407">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1408">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1408">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1409">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1409">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-1410">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1410">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1411">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1411">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1413">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1413">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-1414">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1414">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1416">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1417">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-1418">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1419">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1420">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1421">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1421">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1423">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1423">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1425">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1425">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1427">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1427">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1428">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1428">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1429">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1429">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1430">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1430">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1431">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1431">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1432">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1432">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1433">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1433">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1435">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1435">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1437">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1437">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1439">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1439">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1441">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1441">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-1442">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1442">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1444">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1444">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1445">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1445">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1447">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1447">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1448">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1448">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1449">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1449">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1450">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1450">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-1451">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1451">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1452">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1452">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g8x24_typelesssupvsup-19"></a><span data-ttu-id="937fc-1454">DXGI_FORMAT_R32G8X24_TYPELESS<sup>V</sup> (19)</span><span class="sxs-lookup"><span data-stu-id="937fc-1454">DXGI_FORMAT_R32G8X24_TYPELESS<sup>V</sup> (19)</span></span>
| <span data-ttu-id="937fc-1455">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1455">Target</span></span> | <span data-ttu-id="937fc-1456">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1456">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1457">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1457">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1458">64</span><span class="sxs-lookup"><span data-stu-id="937fc-1458">64</span></span> |
| <span data-ttu-id="937fc-1459">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1459">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1461">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1461">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1462">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1462">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1463">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1463">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1464">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1464">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1465">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1465">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1467">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1467">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1469">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1469">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-1470">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1470">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1472">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1472">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-1473">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1473">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-1474">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1474">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1475">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1475">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1476">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1476">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-1477">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1477">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1478">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1478">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1480">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1480">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-1481">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1481">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1482">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1482">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1483">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1483">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-1484">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1484">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1485">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1485">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1486">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1486">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1487">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1487">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-1488">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1488">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-1489">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1489">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-1490">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1490">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1491">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1491">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1492">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1492">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1493">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1493">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1494">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1494">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1495">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1495">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1496">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1496">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1498">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1498">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1499">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1499">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1500">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1500">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-1501">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1501">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-1502">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1502">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-1503">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1503">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1504">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1504">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1506">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1506">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1507">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1507">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1508">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1508">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1509">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1509">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-1510">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1510">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1511">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1511">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupvsup-20"></a><span data-ttu-id="937fc-1512">DXGI_FORMAT_D32_FLOAT_S8X24_UINT<sup>V</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="937fc-1512">DXGI_FORMAT_D32_FLOAT_S8X24_UINT<sup>V</sup> (20)</span></span>
| <span data-ttu-id="937fc-1513">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1513">Target</span></span> | <span data-ttu-id="937fc-1514">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1514">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1515">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1515">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1516">64</span><span class="sxs-lookup"><span data-stu-id="937fc-1516">64</span></span> |
| <span data-ttu-id="937fc-1517">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1517">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1519">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1519">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1520">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1520">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1521">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1521">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1522">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1522">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1523">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1523">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1525">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1525">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1527">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1527">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-1528">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1528">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1530">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1530">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-1531">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1531">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-1532">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1532">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1533">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1533">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1534">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1534">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-1535">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1535">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1536">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1536">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1538">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1538">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-1539">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1539">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1540">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1540">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1541">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1541">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-1542">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1542">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1544">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1544">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1545">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1545">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1546">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1546">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-1547">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1547">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-1548">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1548">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-1549">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1549">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1550">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1550">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1551">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1551">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1552">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1552">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1553">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1553">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1554">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1554">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1555">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1555">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1557">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1557">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1559">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1559">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1561">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1561">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1563">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1563">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-1564">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1564">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-1565">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1565">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1566">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1566">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1568">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1568">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1569">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1569">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1570">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1570">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1571">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1571">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-1572">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1572">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1573">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1573">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupvsup-21"></a><span data-ttu-id="937fc-1574">DXGI_FORMAT_R32_FLOAT_X8X24_TYPELESS<sup>V</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="937fc-1574">DXGI_FORMAT_R32_FLOAT_X8X24_TYPELESS<sup>V</sup> (21)</span></span>
| <span data-ttu-id="937fc-1575">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1575">Target</span></span> | <span data-ttu-id="937fc-1576">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1576">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1577">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1577">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1578">64</span><span class="sxs-lookup"><span data-stu-id="937fc-1578">64</span></span> |
| <span data-ttu-id="937fc-1579">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1579">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1581">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1581">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1582">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1582">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1583">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1583">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1584">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1584">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1585">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1587">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1589">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-1590">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1590">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1592">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1592">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1594">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1594">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1596">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1596">Shader sample_c (comparison filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1598">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1598">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1599">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1599">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1601">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1601">Shader gather4_c</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1603">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1603">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1605">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1605">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-1606">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1606">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1607">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1607">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1608">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1608">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-1609">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1609">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1610">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1610">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1611">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1611">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1612">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1612">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-1613">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1613">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-1614">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1614">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-1615">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1615">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1616">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1616">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1617">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1617">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1618">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1618">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1619">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1619">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1620">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1620">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1621">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1621">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1623">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1623">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1624">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1624">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1625">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1625">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-1626">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1626">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-1627">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1627">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1629">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1629">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1630">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1630">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1632">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1632">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1633">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1633">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1634">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1634">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1635">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1635">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-1636">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1636">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1637">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1637">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupvsup-22"></a><span data-ttu-id="937fc-1638">DXGI_FORMAT_X32_TYPELESS_G8X24_UINT<sup>V</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="937fc-1638">DXGI_FORMAT_X32_TYPELESS_G8X24_UINT<sup>V</sup> (22)</span></span>
| <span data-ttu-id="937fc-1639">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1639">Target</span></span> | <span data-ttu-id="937fc-1640">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1640">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1641">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1641">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1642">64</span><span class="sxs-lookup"><span data-stu-id="937fc-1642">64</span></span> |
| <span data-ttu-id="937fc-1643">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1643">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1645">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1645">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1646">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1646">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1647">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1647">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1648">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1648">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1649">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1649">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1651">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1651">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1653">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1653">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-1654">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1654">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1656">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1656">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1658">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1658">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-1659">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1659">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1660">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1660">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1661">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1661">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-1662">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1662">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1663">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1663">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1665">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1665">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-1666">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1666">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1667">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1667">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1668">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1668">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-1669">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1669">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1670">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1670">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1671">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1671">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1672">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1672">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-1673">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1673">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-1674">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1674">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-1675">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1675">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1676">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1676">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1677">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1677">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1678">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1678">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1679">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1679">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1680">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1680">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1681">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1681">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1683">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1684">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1685">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-1686">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-1687">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1687">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1689">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1689">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1690">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1690">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1692">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1692">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1693">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1693">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1694">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1694">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1695">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1695">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-1696">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1696">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1697">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1697">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="937fc-1698">DXGI_FORMAT_R10G10B10A2_TYPELESS<sup>PCs</sup> (23)</span><span class="sxs-lookup"><span data-stu-id="937fc-1698">DXGI_FORMAT_R10G10B10A2_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="937fc-1699">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1699">Target</span></span> | <span data-ttu-id="937fc-1700">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1700">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1701">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1701">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1702">32</span><span class="sxs-lookup"><span data-stu-id="937fc-1702">32</span></span> |
| <span data-ttu-id="937fc-1703">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1703">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1705">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1705">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1706">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1706">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1707">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1707">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1708">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1708">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1709">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1709">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1711">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1711">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1713">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1713">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1715">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1715">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1717">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1717">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-1718">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1718">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-1719">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1719">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1720">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1720">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1721">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1721">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-1722">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1722">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1723">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1723">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1725">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1725">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-1726">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1726">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1727">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1727">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1728">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1728">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-1729">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1729">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1730">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1730">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1731">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1731">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1732">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1732">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-1733">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1733">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-1734">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1734">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-1735">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1735">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1736">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1736">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1737">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1737">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1738">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1738">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1739">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1739">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1740">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1740">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1741">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1741">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1743">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1743">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1744">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1744">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1745">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1745">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-1746">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1746">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-1747">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1747">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-1748">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1748">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1749">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1749">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1751">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1751">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1752">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1752">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1753">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1753">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1754">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1754">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1756">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1756">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1757">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1757">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="937fc-1759">DXGI_FORMAT_R10G10B10A2_UNORM<sup>(</sup> 24)</span><span class="sxs-lookup"><span data-stu-id="937fc-1759">DXGI_FORMAT_R10G10B10A2_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="937fc-1760">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1760">Target</span></span> | <span data-ttu-id="937fc-1761">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1761">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1762">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1763">32</span><span class="sxs-lookup"><span data-stu-id="937fc-1763">32</span></span> |
| <span data-ttu-id="937fc-1764">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1764">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1766">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1766">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1768">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1768">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1770">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1771">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1772">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1774">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1774">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1776">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1776">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1778">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1778">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1780">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1780">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1782">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1782">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1784">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1784">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1785">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1785">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1786">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1786">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1788">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1788">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1789">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1789">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1791">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1791">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1793">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1793">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1795">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1795">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1797">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1797">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-1798">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1798">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1799">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1799">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1800">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1800">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1801">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1801">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1803">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1803">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1805">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1805">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1807">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1807">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1808">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1808">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1809">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1809">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1810">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1810">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1811">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1811">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1812">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1812">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1813">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1813">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1815">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1815">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1817">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1817">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1819">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1819">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1821">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1821">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1823">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1823">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1825">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1825">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1827">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1827">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1829">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1829">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1830">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1830">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1832">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1832">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1834">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1834">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1836">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1836">BackBuffer Castable Even Fully Typed</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1838">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1838">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="937fc-1840">DXGI_FORMAT_R10G10B10A2_UINT<sup>(</sup> 25)</span><span class="sxs-lookup"><span data-stu-id="937fc-1840">DXGI_FORMAT_R10G10B10A2_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="937fc-1841">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1841">Target</span></span> | <span data-ttu-id="937fc-1842">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1842">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1843">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1843">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1844">32</span><span class="sxs-lookup"><span data-stu-id="937fc-1844">32</span></span> |
| <span data-ttu-id="937fc-1845">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1845">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1847">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1847">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1849">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1849">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1851">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1851">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1852">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1852">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1853">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1853">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1855">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1855">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1857">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1857">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1859">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1859">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1861">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1861">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1863">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1863">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-1864">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1864">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1865">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1865">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1866">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1866">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-1867">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1867">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1868">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1868">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1870">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1870">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-1871">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1871">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1873">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1873">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1874">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1874">Output Merger Logic Op</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1876">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1876">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1877">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1877">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1878">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1878">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1879">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1879">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1881">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1881">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1883">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1883">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1885">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1885">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1886">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1886">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1887">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1887">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1888">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1888">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1889">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1889">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1890">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1890">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1891">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1891">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1893">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1893">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1895">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1895">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1897">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1897">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1899">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1899">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-1900">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1900">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1902">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1902">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-1903">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1903">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1905">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1906">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-1907">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-1908">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1908">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1910">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1910">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-1911">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1911">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="937fc-1913">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM<sup>(</sup> 89)</span><span class="sxs-lookup"><span data-stu-id="937fc-1913">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="937fc-1914">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1914">Target</span></span> | <span data-ttu-id="937fc-1915">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1915">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1916">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1916">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1917">32</span><span class="sxs-lookup"><span data-stu-id="937fc-1917">32</span></span> |
| <span data-ttu-id="937fc-1918">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1918">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1920">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1920">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1921">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1921">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1922">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1922">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1923">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1923">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1924">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1924">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-1925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1925">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1927">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-1928">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1928">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-1929">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1929">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-1930">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1930">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-1931">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1931">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-1932">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1932">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-1933">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-1933">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-1934">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-1934">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-1935">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1935">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-1936">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-1936">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-1937">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1937">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1938">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1938">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1939">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-1939">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-1940">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1940">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-1941">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1941">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1942">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-1942">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-1943">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-1943">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-1944">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-1944">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-1945">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1945">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-1946">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-1946">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-1947">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-1947">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-1948">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-1948">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-1949">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-1949">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-1950">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-1950">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1951">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-1951">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-1952">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-1952">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1954">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1954">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1955">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-1955">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-1956">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-1956">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-1957">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-1957">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-1958">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-1958">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-1959">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-1959">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1961">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-1961">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1963">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-1963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-1964">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1964">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-1966">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-1966">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1968">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1968">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1970">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-1970">BackBuffer Castable Even Fully Typed</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1972">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-1972">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="937fc-1974">DXGI_FORMAT_R11G11B10_FLOAT<sup>(</sup> 26)</span><span class="sxs-lookup"><span data-stu-id="937fc-1974">DXGI_FORMAT_R11G11B10_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="937fc-1975">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-1975">Target</span></span> | <span data-ttu-id="937fc-1976">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-1976">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-1977">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-1977">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-1978">32</span><span class="sxs-lookup"><span data-stu-id="937fc-1978">32</span></span> |
| <span data-ttu-id="937fc-1979">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-1979">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1981">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1981">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1983">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-1983">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1985">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-1985">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1986">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-1986">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-1987">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-1987">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1989">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-1989">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1991">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-1991">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1993">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-1993">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1995">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-1995">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1997">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1997">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-1999">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-1999">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2000">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2000">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2001">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2001">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2003">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2003">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2004">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2004">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2006">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2006">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2008">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2008">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2010">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2010">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2012">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-2013">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2014">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2015">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2016">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2016">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2018">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2018">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2020">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2020">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2022">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2022">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2023">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2023">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2024">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2024">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2025">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2025">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2026">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2026">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2027">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2027">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2028">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2028">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2030">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2030">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2032">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2032">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2034">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2034">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2036">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2036">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2038">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2038">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2040">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2040">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-2041">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2041">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-2042">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2042">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2043">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2043">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-2044">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2044">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-2045">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2045">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-2046">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2046">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-2047">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2047">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="937fc-2049">DXGI_FORMAT_R8G8B8A8_TYPELESS<sup>PCs</sup> (27)</span><span class="sxs-lookup"><span data-stu-id="937fc-2049">DXGI_FORMAT_R8G8B8A8_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="937fc-2050">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2050">Target</span></span> | <span data-ttu-id="937fc-2051">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2051">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2052">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2052">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2053">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2053">32</span></span> |
| <span data-ttu-id="937fc-2054">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2054">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2056">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2056">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2057">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2057">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2058">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2058">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2059">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2059">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2060">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2060">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2062">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2062">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2064">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2064">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2066">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2066">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2068">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2068">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-2069">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2069">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-2070">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2070">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2071">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2071">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2072">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2072">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-2073">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2073">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2074">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2074">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2076">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2076">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-2077">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2077">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2078">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2078">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2079">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2079">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-2080">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2080">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2081">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2081">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2082">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2082">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2083">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2083">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-2084">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2084">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-2085">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2085">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-2086">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2086">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2087">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2087">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2088">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2088">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2089">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2089">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2090">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2090">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2091">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2091">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2092">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2092">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2094">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2094">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2095">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2095">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2096">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2096">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-2097">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2097">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-2098">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2098">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-2099">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2099">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-2100">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2100">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2102">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2102">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2103">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2103">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-2104">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2104">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-2105">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2105">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2107">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2107">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-2108">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2108">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="937fc-2110">DXGI_FORMAT_R8G8B8A8_UNORM<sup>(</sup> 28)</span><span class="sxs-lookup"><span data-stu-id="937fc-2110">DXGI_FORMAT_R8G8B8A8_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="937fc-2111">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2111">Target</span></span> | <span data-ttu-id="937fc-2112">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2112">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2113">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2113">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2114">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2114">32</span></span> |
| <span data-ttu-id="937fc-2115">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2115">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2117">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2117">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2119">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2119">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2121">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2121">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2122">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2122">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2123">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2123">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2125">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2125">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2127">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2127">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2129">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2129">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2131">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2131">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2133">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2133">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2135">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2135">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2136">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2136">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2137">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2137">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2139">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2139">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2140">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2140">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2142">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2142">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2144">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2144">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2146">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2146">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2148">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2148">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-2149">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2149">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2150">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2150">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2151">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2151">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2152">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2152">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2154">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2154">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2156">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2156">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2158">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2158">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2159">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2159">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2160">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2160">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2161">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2161">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2162">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2162">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2163">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2163">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2164">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2164">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2166">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2166">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2168">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2168">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2170">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2170">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2172">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2172">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2174">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2174">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2176">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2176">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2178">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2178">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2180">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2180">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2181">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2181">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2183">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2183">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2185">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2185">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2187">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2187">BackBuffer Castable Even Fully Typed</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2189">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2189">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="937fc-2191">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB<sup>(</sup> 29)</span><span class="sxs-lookup"><span data-stu-id="937fc-2191">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="937fc-2192">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2192">Target</span></span> | <span data-ttu-id="937fc-2193">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2193">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2194">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2194">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2195">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2195">32</span></span> |
| <span data-ttu-id="937fc-2196">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2196">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2198">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2198">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2199">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2199">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2200">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2200">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2201">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2201">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2202">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2202">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2204">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2204">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2206">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2206">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2208">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2208">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2210">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2210">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2212">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2212">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2214">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2214">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2215">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2215">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2216">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2216">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2218">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2218">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2219">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2219">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2221">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2221">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2223">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2225">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2225">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2227">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2227">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-2228">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2228">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2229">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2229">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2230">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2230">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2231">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2231">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-2232">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2232">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-2233">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2233">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-2234">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2234">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2235">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2235">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2236">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2236">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2237">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2237">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2238">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2238">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2239">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2239">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2240">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2240">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2242">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2242">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2244">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2244">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2246">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2246">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2248">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2248">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2250">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2250">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2252">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2252">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2254">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2254">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2256">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2256">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2257">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2257">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2259">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2259">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2261">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2261">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2263">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2263">BackBuffer Castable Even Fully Typed</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2265">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2265">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="937fc-2267">DXGI_FORMAT_R8G8B8A8_UINT-(<sup>e</sup> )</span><span class="sxs-lookup"><span data-stu-id="937fc-2267">DXGI_FORMAT_R8G8B8A8_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="937fc-2268">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2268">Target</span></span> | <span data-ttu-id="937fc-2269">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2269">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2270">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2270">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2271">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2271">32</span></span> |
| <span data-ttu-id="937fc-2272">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2272">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2274">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2274">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2276">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2276">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2278">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2278">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2279">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2279">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2280">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2280">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2282">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2282">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2284">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2284">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2286">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2288">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2288">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2290">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2290">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-2291">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2291">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2292">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2292">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2293">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2293">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-2294">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2294">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2295">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2295">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2297">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2297">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-2298">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2298">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2300">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2300">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2301">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2301">Output Merger Logic Op</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2303">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2304">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2305">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2306">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2306">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2308">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2308">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2310">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2310">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2312">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2312">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2313">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2313">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2314">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2314">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2315">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2315">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2316">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2316">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2317">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2317">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2318">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2318">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2320">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2320">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2322">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2322">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2324">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2324">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2326">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2326">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-2327">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2327">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2329">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2329">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-2330">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2330">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2332">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2332">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2333">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2333">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-2334">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2334">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-2335">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2335">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2337">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2337">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-2338">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2338">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="937fc-2340">DXGI_FORMAT_R8G8B8A8_SNORM<sup>(</sup> 31)</span><span class="sxs-lookup"><span data-stu-id="937fc-2340">DXGI_FORMAT_R8G8B8A8_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="937fc-2341">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2341">Target</span></span> | <span data-ttu-id="937fc-2342">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2342">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2343">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2343">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2344">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2344">32</span></span> |
| <span data-ttu-id="937fc-2345">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2345">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2347">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2347">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2349">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2349">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2351">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2352">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2353">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2355">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2355">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2357">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2357">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2359">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2359">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2361">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2361">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2363">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2363">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2365">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2365">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2366">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2366">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2367">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2367">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2369">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2369">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2370">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2370">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2372">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2372">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2374">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2374">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2376">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2376">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2378">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2378">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-2379">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2379">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2380">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2380">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2381">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2381">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2382">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2382">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2384">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2384">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2386">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2386">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2388">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2388">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2389">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2389">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2390">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2390">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2391">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2391">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2392">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2392">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2393">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2393">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2394">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2394">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2396">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2396">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2398">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2398">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2400">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2400">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2402">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2402">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2404">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2404">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2406">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2406">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-2407">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2407">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2409">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2409">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2410">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2410">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-2411">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2411">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-2412">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2412">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2414">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2414">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-2415">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2415">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="937fc-2417">DXGI_FORMAT_R8G8B8A8_SINT<sup>(</sup> 32)</span><span class="sxs-lookup"><span data-stu-id="937fc-2417">DXGI_FORMAT_R8G8B8A8_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="937fc-2418">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2418">Target</span></span> | <span data-ttu-id="937fc-2419">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2419">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2420">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2420">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2421">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2421">32</span></span> |
| <span data-ttu-id="937fc-2422">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2422">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2424">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2424">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2426">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2426">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2428">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2428">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2429">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2429">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2430">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2430">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2432">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2432">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2434">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2434">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2436">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2436">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2438">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2438">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2440">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-2441">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2441">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2442">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2442">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2443">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2443">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-2444">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2444">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2445">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2445">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2447">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2447">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-2448">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2448">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2450">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2450">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2451">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2451">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-2452">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2452">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2453">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2453">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2454">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2454">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2455">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2455">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2457">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2457">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2459">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2459">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2461">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2461">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2462">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2462">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2463">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2463">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2464">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2464">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2465">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2465">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2466">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2466">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2467">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2467">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2469">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2469">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2471">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2471">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2473">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2473">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2475">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2475">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-2476">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2476">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2478">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-2479">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2479">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2481">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2482">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-2483">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-2484">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2484">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2486">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2486">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-2487">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2487">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="937fc-2489">DXGI_FORMAT_R16G16_TYPELESS<sup>PCs</sup> (33)</span><span class="sxs-lookup"><span data-stu-id="937fc-2489">DXGI_FORMAT_R16G16_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="937fc-2490">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2490">Target</span></span> | <span data-ttu-id="937fc-2491">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2491">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2492">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2492">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2493">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2493">32</span></span> |
| <span data-ttu-id="937fc-2494">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2494">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2496">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2496">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2497">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2498">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2499">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2500">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2502">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2502">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2504">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2506">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2508">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2508">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-2509">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2509">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-2510">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2510">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2511">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2511">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2512">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2512">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-2513">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2513">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2514">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2514">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2516">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2516">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-2517">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2517">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2518">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2518">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2519">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2519">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-2520">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2520">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2521">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2521">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2522">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2522">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2523">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2523">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-2524">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2524">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-2525">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2525">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-2526">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2526">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2527">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2527">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2528">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2528">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2529">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2529">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2530">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2530">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2531">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2531">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2532">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2532">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2534">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2534">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2535">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2535">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2536">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2536">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-2537">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2537">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-2538">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2538">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-2539">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2539">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-2540">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2540">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2542">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2542">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2543">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2543">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-2544">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2544">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-2545">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2545">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-2546">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2546">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-2547">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2547">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="937fc-2549">DXGI_FORMAT_R16G16_FLOAT<sup>(</sup> 34)</span><span class="sxs-lookup"><span data-stu-id="937fc-2549">DXGI_FORMAT_R16G16_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="937fc-2550">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2550">Target</span></span> | <span data-ttu-id="937fc-2551">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2551">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2552">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2552">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2553">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2553">32</span></span> |
| <span data-ttu-id="937fc-2554">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2554">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2556">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2556">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2558">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2558">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2560">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2560">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2561">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2561">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2562">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2562">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2564">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2564">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2566">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2568">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2568">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2570">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2570">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2572">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2572">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2574">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2574">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2575">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2575">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2576">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2576">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2578">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2578">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2579">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2579">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2581">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2581">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2583">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2583">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2585">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2585">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2587">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2587">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-2588">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2588">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2589">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2589">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2590">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2590">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2591">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2591">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2593">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2593">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2595">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2595">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2597">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2597">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2598">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2598">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2599">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2599">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2600">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2600">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2601">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2601">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2602">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2602">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2603">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2603">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2605">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2605">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2607">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2607">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2609">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2609">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2611">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2611">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2613">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2613">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2615">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2615">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-2616">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2616">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2618">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2618">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2619">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2619">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-2620">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2620">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-2621">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2621">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-2622">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2622">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-2623">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2623">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="937fc-2625">DXGI_FORMAT_R16G16_UNORM<sup>(</sup> 35)</span><span class="sxs-lookup"><span data-stu-id="937fc-2625">DXGI_FORMAT_R16G16_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="937fc-2626">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2626">Target</span></span> | <span data-ttu-id="937fc-2627">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2627">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2628">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2628">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2629">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2629">32</span></span> |
| <span data-ttu-id="937fc-2630">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2630">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2632">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2632">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2634">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2634">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2636">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2636">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2637">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2637">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2638">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2638">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2640">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2642">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2644">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2644">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2646">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2646">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2648">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2648">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2650">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2650">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2651">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2651">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2652">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2652">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2654">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2654">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2655">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2655">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2657">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2657">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2659">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2659">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2661">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2661">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2663">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2663">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-2664">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2664">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2665">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2665">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2666">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2666">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2667">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2667">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2669">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2669">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2671">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2671">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2673">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2673">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2674">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2674">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2675">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2675">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2676">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2676">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2677">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2677">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2678">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2678">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2679">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2679">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2681">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2681">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2683">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2683">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2685">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2685">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2687">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2687">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2689">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2689">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2691">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2691">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-2692">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2692">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2694">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2694">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2695">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2695">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-2696">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2696">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-2697">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2697">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-2698">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2698">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-2699">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2699">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="937fc-2701">DXGI_FORMAT_R16G16_UINT<sup>(</sup> 36)</span><span class="sxs-lookup"><span data-stu-id="937fc-2701">DXGI_FORMAT_R16G16_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="937fc-2702">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2702">Target</span></span> | <span data-ttu-id="937fc-2703">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2703">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2704">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2704">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2705">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2705">32</span></span> |
| <span data-ttu-id="937fc-2706">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2706">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2708">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2708">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2710">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2710">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2712">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2712">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2713">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2713">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2714">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2714">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2716">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2718">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2720">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2722">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2722">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2724">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2724">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-2725">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2725">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2726">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2726">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2727">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2727">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-2728">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2728">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2729">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2729">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2731">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2731">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-2732">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2732">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2734">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2734">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2735">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2735">Output Merger Logic Op</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2737">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2738">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2739">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2740">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2740">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2742">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2742">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2744">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2744">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2746">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2746">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2747">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2747">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2748">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2748">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2749">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2749">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2750">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2750">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2751">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2751">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2752">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2752">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2754">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2754">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2756">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2756">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2758">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2758">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2760">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2760">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-2761">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2761">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2763">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2763">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-2764">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2764">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2766">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2766">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2767">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2767">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-2768">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2768">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-2769">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2769">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-2770">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2770">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-2771">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2771">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="937fc-2773">DXGI_FORMAT_R16G16_SNORM<sup>(</sup> 37)</span><span class="sxs-lookup"><span data-stu-id="937fc-2773">DXGI_FORMAT_R16G16_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="937fc-2774">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2774">Target</span></span> | <span data-ttu-id="937fc-2775">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2775">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2776">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2776">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2777">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2777">32</span></span> |
| <span data-ttu-id="937fc-2778">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2778">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2780">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2780">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2782">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2782">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2784">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2784">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2785">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2785">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2786">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2786">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2788">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2788">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2790">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2790">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2792">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2792">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2794">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2794">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2796">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2796">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2798">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2798">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2799">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2799">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2800">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2800">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2802">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2802">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2803">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2803">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2805">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2805">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2807">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2809">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2809">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2811">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-2812">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2813">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2814">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2815">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2815">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2817">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2817">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2819">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2819">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2821">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2821">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2822">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2822">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2823">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2823">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2824">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2824">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2825">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2825">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2826">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2826">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2827">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2827">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2829">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2829">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2831">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2831">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2833">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2833">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2835">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2835">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2837">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2837">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2839">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2839">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-2840">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2840">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2842">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2842">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2843">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2843">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-2844">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2844">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-2845">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2845">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-2846">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2846">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-2847">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2847">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="937fc-2849">DXGI_FORMAT_R16G16_SINT<sup>(</sup> 38)</span><span class="sxs-lookup"><span data-stu-id="937fc-2849">DXGI_FORMAT_R16G16_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="937fc-2850">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2850">Target</span></span> | <span data-ttu-id="937fc-2851">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2851">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2852">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2852">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2853">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2853">32</span></span> |
| <span data-ttu-id="937fc-2854">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2854">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2856">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2856">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2858">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2858">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2860">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2861">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2862">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2864">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2864">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2866">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2866">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2868">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2870">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2870">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2872">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2872">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-2873">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2873">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2874">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2874">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2875">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2875">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-2876">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2876">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2877">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2877">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2879">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2879">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-2880">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2880">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2882">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2883">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-2884">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2885">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2886">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2887">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2887">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2889">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2889">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2891">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2891">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2893">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2893">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2894">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2894">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2895">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2895">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2896">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2896">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2897">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2897">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2898">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2898">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2899">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2899">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2901">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2901">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2903">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2903">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2905">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2905">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-2907">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2907">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-2908">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2908">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2910">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2910">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-2911">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2911">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2913">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2914">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-2915">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-2916">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-2917">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2917">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-2918">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2918">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="937fc-2920">DXGI_FORMAT_R32_TYPELESS<sup>PCs</sup> (39)</span><span class="sxs-lookup"><span data-stu-id="937fc-2920">DXGI_FORMAT_R32_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="937fc-2921">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2921">Target</span></span> | <span data-ttu-id="937fc-2922">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2922">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2923">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2923">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2924">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2924">32</span></span> |
| <span data-ttu-id="937fc-2925">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2925">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2927">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2927">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2928">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2928">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2929">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2929">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2930">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2930">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2931">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2931">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2933">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2933">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2935">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2935">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2937">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2937">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2939">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-2939">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-2940">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2940">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-2941">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2941">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-2942">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-2942">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-2943">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-2943">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-2944">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-2944">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-2945">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2945">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2947">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-2947">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-2948">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2948">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2949">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2949">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2950">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-2950">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-2951">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2951">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-2952">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2952">Raw UAV and SRV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2954">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-2954">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-2955">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-2955">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-2956">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-2956">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-2957">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2957">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-2958">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-2958">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-2959">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-2959">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-2960">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-2960">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-2961">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-2961">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-2962">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-2962">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2963">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-2963">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-2964">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-2964">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2966">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2966">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2967">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-2967">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-2968">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-2968">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-2969">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-2969">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-2970">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-2970">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-2971">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-2971">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-2972">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-2972">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2974">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-2974">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-2975">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2975">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-2976">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-2976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-2977">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2977">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2979">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-2979">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-2980">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-2980">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="937fc-2982">DXGI_FORMAT_D32_FLOAT<sup>(</sup> 40)</span><span class="sxs-lookup"><span data-stu-id="937fc-2982">DXGI_FORMAT_D32_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="937fc-2983">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-2983">Target</span></span> | <span data-ttu-id="937fc-2984">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-2984">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-2985">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-2985">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-2986">32</span><span class="sxs-lookup"><span data-stu-id="937fc-2986">32</span></span> |
| <span data-ttu-id="937fc-2987">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-2987">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2989">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2989">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2990">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-2990">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2991">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-2991">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2992">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-2992">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-2993">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-2993">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2995">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-2995">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-2997">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-2997">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-2998">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-2998">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3000">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3000">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-3001">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3001">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-3002">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3002">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3003">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3003">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3004">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3004">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-3005">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3005">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3006">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3006">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3008">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3008">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-3009">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3009">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3010">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3010">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3011">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3011">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3012">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3012">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3014">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3015">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3016">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3016">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-3017">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-3018">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-3019">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3020">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3021">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3022">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-3023">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3023">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3024">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3024">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3025">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3025">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3027">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3027">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3029">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3029">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3031">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3031">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3033">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3033">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-3034">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3034">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-3035">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3035">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3036">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3036">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3038">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3038">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3039">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3039">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3040">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3040">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3041">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3041">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3043">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3043">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3044">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3044">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="937fc-3046">DXGI_FORMAT_R32_FLOAT<sup>(</sup> 41)</span><span class="sxs-lookup"><span data-stu-id="937fc-3046">DXGI_FORMAT_R32_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="937fc-3047">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3047">Target</span></span> | <span data-ttu-id="937fc-3048">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3048">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3049">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3049">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3050">32</span><span class="sxs-lookup"><span data-stu-id="937fc-3050">32</span></span> |
| <span data-ttu-id="937fc-3051">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3051">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3053">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3053">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3055">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3055">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3057">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3057">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3058">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3058">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3060">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3060">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3062">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3062">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3064">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3064">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3066">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3066">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3068">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3068">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3070">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3070">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3072">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3072">Shader sample_c (comparison filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3074">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3074">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3075">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3075">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3077">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3077">Shader gather4_c</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3079">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3079">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3081">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3081">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3083">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3083">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3085">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3085">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3087">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3088">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3089">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3090">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3091">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3091">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3093">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3093">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3095">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3095">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3097">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3097">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3098">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3098">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3099">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3099">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3100">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3100">UAV Atomic Exchange</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3102">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3102">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3103">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3103">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3104">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3104">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3106">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3106">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3108">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3108">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3110">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3110">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3112">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3112">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3114">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3114">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3116">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3116">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3117">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3117">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3119">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3120">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3121">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3122">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3122">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3124">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3124">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3125">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3125">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="937fc-3127">DXGI_FORMAT_R32_UINT<sup>(</sup> 42)</span><span class="sxs-lookup"><span data-stu-id="937fc-3127">DXGI_FORMAT_R32_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="937fc-3128">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3128">Target</span></span> | <span data-ttu-id="937fc-3129">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3129">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3130">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3131">32</span><span class="sxs-lookup"><span data-stu-id="937fc-3131">32</span></span> |
| <span data-ttu-id="937fc-3132">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3132">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3134">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3134">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3136">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3136">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3138">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3138">Input Assembler Index Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3140">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3140">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3142">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3144">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3146">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3148">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3148">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3150">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3150">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3152">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3152">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-3153">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3153">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3154">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3154">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3155">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3155">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-3156">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3156">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3157">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3157">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3159">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3159">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-3160">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3160">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3162">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3163">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3163">Output Merger Logic Op</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3165">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3165">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3166">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3166">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3167">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3167">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3168">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3168">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3170">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3170">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3172">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3172">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3174">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3174">UAV Atomic Add</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3176">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3176">UAV Atomic Bitwise Ops</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3178">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3178">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3180">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3180">UAV Atomic Exchange</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3182">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3182">UAV Atomic Signed Min/Max</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3184">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3184">UAV Atomic Unsigned Min/Max</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3186">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3186">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3188">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3188">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3190">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3190">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3192">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3192">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3194">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3194">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-3195">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3195">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3197">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3197">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3198">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3198">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3200">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3200">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3201">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3201">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3202">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3202">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3203">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3203">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3205">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3205">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3206">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3206">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="937fc-3208">DXGI_FORMAT_R32_SINT<sup>(</sup> 43)</span><span class="sxs-lookup"><span data-stu-id="937fc-3208">DXGI_FORMAT_R32_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="937fc-3209">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3209">Target</span></span> | <span data-ttu-id="937fc-3210">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3210">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3211">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3211">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3212">32</span><span class="sxs-lookup"><span data-stu-id="937fc-3212">32</span></span> |
| <span data-ttu-id="937fc-3213">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3213">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3215">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3215">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3217">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3217">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3219">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3219">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3220">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3220">Stream Output Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3222">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3222">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3224">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3224">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3226">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3226">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3228">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3228">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3230">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3230">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3232">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3232">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-3233">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3233">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3234">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3234">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3235">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3235">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-3236">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3236">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3237">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3237">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3239">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3239">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-3240">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3240">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3242">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3242">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3243">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3243">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3244">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3244">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3245">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3245">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3246">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3246">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3247">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3247">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3249">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3249">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3251">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3251">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3253">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3253">UAV Atomic Add</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3255">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3255">UAV Atomic Bitwise Ops</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3257">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3257">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3259">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3259">UAV Atomic Exchange</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3261">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3261">UAV Atomic Signed Min/Max</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3263">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3263">UAV Atomic Unsigned Min/Max</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3265">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3265">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3267">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3267">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3269">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3269">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3271">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3271">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3273">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3273">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-3274">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3274">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3276">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3276">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3277">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3277">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3279">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3279">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3280">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3280">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3281">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3281">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3282">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3282">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3284">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3284">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3285">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3285">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r24g8_typelesssupvsup-44"></a><span data-ttu-id="937fc-3287">DXGI_FORMAT_R24G8_TYPELESS<sup>V</sup> (44)</span><span class="sxs-lookup"><span data-stu-id="937fc-3287">DXGI_FORMAT_R24G8_TYPELESS<sup>V</sup> (44)</span></span>
| <span data-ttu-id="937fc-3288">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3288">Target</span></span> | <span data-ttu-id="937fc-3289">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3289">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3290">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3290">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3291">32</span><span class="sxs-lookup"><span data-stu-id="937fc-3291">32</span></span> |
| <span data-ttu-id="937fc-3292">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3292">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3294">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3294">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3295">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3295">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3296">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3296">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3297">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3297">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3298">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3298">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3300">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3302">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3302">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-3303">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3303">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3305">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3305">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-3306">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3306">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-3307">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3307">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3308">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3308">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3309">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3309">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-3310">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3310">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3311">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3311">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3313">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3313">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-3314">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3314">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3315">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3315">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3316">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3316">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3317">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3317">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3318">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3318">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3319">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3319">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3320">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3320">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-3321">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3321">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-3322">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3322">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-3323">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3323">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3324">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3324">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3325">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3325">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3326">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3326">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-3327">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3327">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3328">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3328">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3329">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3329">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3331">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3332">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3333">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-3334">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-3335">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3335">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-3336">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3337">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3337">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3339">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3339">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3340">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3340">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3341">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3341">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3342">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3342">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-3343">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3343">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3344">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3344">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupvsup-45"></a><span data-ttu-id="937fc-3345">DXGI_FORMAT_D24_UNORM_S8_UINT<sup>V</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="937fc-3345">DXGI_FORMAT_D24_UNORM_S8_UINT<sup>V</sup> (45)</span></span>
| <span data-ttu-id="937fc-3346">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3346">Target</span></span> | <span data-ttu-id="937fc-3347">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3347">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3348">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3348">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3349">32</span><span class="sxs-lookup"><span data-stu-id="937fc-3349">32</span></span> |
| <span data-ttu-id="937fc-3350">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3350">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3352">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3352">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3353">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3353">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3354">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3354">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3355">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3355">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3356">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3356">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3358">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3358">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3360">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-3361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3361">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3363">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3363">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-3364">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3364">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-3365">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3365">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3366">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3366">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3367">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3367">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-3368">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3368">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3369">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3369">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3371">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3371">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-3372">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3372">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3373">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3373">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3374">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3375">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3375">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3377">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3377">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3378">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3378">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3379">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3379">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-3380">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3380">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-3381">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3381">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-3382">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3382">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3383">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3383">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3384">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3384">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3385">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3385">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-3386">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3386">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3387">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3387">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3388">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3388">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3390">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3390">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3392">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3392">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3394">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3394">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3396">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3396">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-3397">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3397">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-3398">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3398">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3399">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3399">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3401">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3401">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3402">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3402">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3403">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3403">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3404">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3404">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-3405">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3405">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3406">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3406">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupvsup-46"></a><span data-ttu-id="937fc-3407">DXGI_FORMAT_R24_UNORM_X8_TYPELESS<sup>V</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="937fc-3407">DXGI_FORMAT_R24_UNORM_X8_TYPELESS<sup>V</sup> (46)</span></span>
| <span data-ttu-id="937fc-3408">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3408">Target</span></span> | <span data-ttu-id="937fc-3409">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3409">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3410">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3410">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3411">32</span><span class="sxs-lookup"><span data-stu-id="937fc-3411">32</span></span> |
| <span data-ttu-id="937fc-3412">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3412">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3414">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3414">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3415">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3415">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3416">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3416">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3417">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3417">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3418">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3418">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3420">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3420">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3422">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3422">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-3423">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3423">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3425">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3425">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3427">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3427">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3429">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3429">Shader sample_c (comparison filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3431">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3431">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3432">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3432">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3434">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3434">Shader gather4_c</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3436">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3436">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3438">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3438">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-3439">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3439">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3440">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3440">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3441">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3441">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3442">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3442">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3443">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3443">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3444">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3444">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3445">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3445">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-3446">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3446">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-3447">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3447">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-3448">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3448">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3449">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3449">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3450">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3450">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3451">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3451">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-3452">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3452">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3453">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3453">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3454">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3454">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3456">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3456">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3457">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3457">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3458">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3458">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-3459">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3459">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-3460">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3460">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3462">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3462">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3463">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3463">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3465">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3465">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3466">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3466">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3467">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3467">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3468">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3468">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-3469">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3469">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3470">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3470">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupvsup-47"></a><span data-ttu-id="937fc-3471">DXGI_FORMAT_X24_TYPELESS_G8_UINT<sup>V</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="937fc-3471">DXGI_FORMAT_X24_TYPELESS_G8_UINT<sup>V</sup> (47)</span></span>
| <span data-ttu-id="937fc-3472">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3472">Target</span></span> | <span data-ttu-id="937fc-3473">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3473">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3474">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3474">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3475">32</span><span class="sxs-lookup"><span data-stu-id="937fc-3475">32</span></span> |
| <span data-ttu-id="937fc-3476">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3476">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3478">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3478">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3479">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3479">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3480">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3480">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3481">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3481">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3482">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3482">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3484">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3484">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3486">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3486">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-3487">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3487">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3489">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3489">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3491">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3491">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-3492">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3492">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3493">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3493">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3494">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3494">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-3495">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3495">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3496">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3496">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3498">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3498">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-3499">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3499">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3500">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3500">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3501">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3501">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3502">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3502">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3503">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3503">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3504">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3504">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3505">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3505">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-3506">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3506">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-3507">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3507">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-3508">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3508">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3509">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3509">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3510">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3510">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3511">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3511">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-3512">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3512">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3513">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3513">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3514">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3514">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3516">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3516">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3517">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3517">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3518">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3518">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-3519">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3519">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-3520">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3520">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3522">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3522">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3523">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3523">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3525">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3526">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3527">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3528">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3528">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-3529">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3529">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3530">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3530">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="937fc-3531">DXGI_FORMAT_R8G8_TYPELESS<sup>PCs</sup> (48)</span><span class="sxs-lookup"><span data-stu-id="937fc-3531">DXGI_FORMAT_R8G8_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="937fc-3532">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3532">Target</span></span> | <span data-ttu-id="937fc-3533">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3533">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3534">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3534">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3535">16</span><span class="sxs-lookup"><span data-stu-id="937fc-3535">16</span></span> |
| <span data-ttu-id="937fc-3536">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3536">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3538">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3538">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3539">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3539">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3540">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3540">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3541">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3541">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3542">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3542">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3544">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3544">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3546">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3546">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3548">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3548">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3550">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3550">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-3551">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3551">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-3552">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3552">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3553">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3553">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3554">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3554">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-3555">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3555">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3556">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3556">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3558">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3558">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-3559">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3559">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3560">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3560">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3561">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3561">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3562">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3562">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3563">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3563">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3564">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3564">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3565">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3565">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-3566">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3566">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-3567">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3567">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-3568">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3568">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3569">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3569">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3570">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3570">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3571">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3571">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-3572">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3572">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3573">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3573">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3574">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3574">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3576">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3576">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3577">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3577">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3578">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3578">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-3579">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3579">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-3580">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3580">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-3581">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3581">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3582">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3582">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3584">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3584">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3585">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3585">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3586">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3586">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3587">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3587">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-3588">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3588">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3589">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3589">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="937fc-3591">DXGI_FORMAT_R8G8_UNORM<sup>(</sup> 49)</span><span class="sxs-lookup"><span data-stu-id="937fc-3591">DXGI_FORMAT_R8G8_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="937fc-3592">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3592">Target</span></span> | <span data-ttu-id="937fc-3593">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3593">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3594">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3594">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3595">16</span><span class="sxs-lookup"><span data-stu-id="937fc-3595">16</span></span> |
| <span data-ttu-id="937fc-3596">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3596">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3598">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3598">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3600">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3600">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3602">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3602">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3603">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3603">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3604">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3604">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3606">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3608">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3608">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3610">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3612">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3612">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3614">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3614">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3616">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3616">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3617">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3617">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3618">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3618">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3620">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3620">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3621">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3621">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3623">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3623">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3625">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3625">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3627">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3627">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3629">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3629">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3630">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3630">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3631">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3631">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3632">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3632">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3633">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3633">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3635">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3635">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3637">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3637">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3639">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3639">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3640">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3640">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3641">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3641">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3642">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3642">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-3643">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3643">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3644">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3644">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3645">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3645">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3647">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3647">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3649">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3649">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3651">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3651">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3653">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3653">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3655">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3655">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3657">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3658">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3658">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3660">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3660">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3661">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3661">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3662">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3662">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3663">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3663">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3665">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3665">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3666">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3666">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="937fc-3668">DXGI_FORMAT_R8G8_UINT<sup>(</sup> 50)</span><span class="sxs-lookup"><span data-stu-id="937fc-3668">DXGI_FORMAT_R8G8_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="937fc-3669">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3669">Target</span></span> | <span data-ttu-id="937fc-3670">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3670">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3671">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3671">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3672">16</span><span class="sxs-lookup"><span data-stu-id="937fc-3672">16</span></span> |
| <span data-ttu-id="937fc-3673">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3673">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3675">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3675">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3677">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3677">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3679">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3679">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3680">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3680">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3681">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3681">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3683">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3683">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3685">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3685">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3687">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3687">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3689">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3689">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3691">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3691">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-3692">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3692">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3693">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3693">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3694">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3694">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-3695">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3695">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3696">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3696">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3698">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3698">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-3699">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3699">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3701">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3701">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3702">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3702">Output Merger Logic Op</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3704">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3704">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3705">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3705">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3706">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3706">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3707">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3707">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3709">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3709">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3711">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3711">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3713">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3713">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3714">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3714">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3715">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3715">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3716">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3716">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-3717">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3717">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3718">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3718">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3719">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3719">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3721">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3721">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3723">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3723">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3725">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3725">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3727">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3727">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-3728">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3728">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3730">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3730">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3731">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3731">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3733">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3733">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3734">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3734">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3735">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3735">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3736">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3736">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-3737">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3737">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3738">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3738">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="937fc-3740">DXGI_FORMAT_R8G8_SNORM<sup>(</sup> 51)</span><span class="sxs-lookup"><span data-stu-id="937fc-3740">DXGI_FORMAT_R8G8_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="937fc-3741">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3741">Target</span></span> | <span data-ttu-id="937fc-3742">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3742">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3743">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3743">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3744">16</span><span class="sxs-lookup"><span data-stu-id="937fc-3744">16</span></span> |
| <span data-ttu-id="937fc-3745">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3745">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3747">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3747">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3749">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3749">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3751">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3751">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3752">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3752">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3753">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3753">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3755">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3755">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3757">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3759">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3759">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3761">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3761">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3763">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3763">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3765">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3765">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3766">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3766">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3767">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3767">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3769">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3769">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3770">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3770">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3772">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3772">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3774">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3774">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3776">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3776">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3778">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3778">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3779">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3779">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3780">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3780">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3781">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3781">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3782">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3782">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3784">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3784">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3786">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3786">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3788">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3788">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3789">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3789">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3790">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3790">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3791">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3791">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-3792">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3792">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3793">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3793">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3794">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3794">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3796">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3796">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3798">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3798">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3800">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3800">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3802">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3802">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3804">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3804">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3806">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3806">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3807">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3807">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3809">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3809">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3810">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3810">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3811">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3811">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3812">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3812">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-3813">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3813">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3814">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3814">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="937fc-3816">DXGI_FORMAT_R8G8_SINT<sup>(</sup> 52)</span><span class="sxs-lookup"><span data-stu-id="937fc-3816">DXGI_FORMAT_R8G8_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="937fc-3817">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3817">Target</span></span> | <span data-ttu-id="937fc-3818">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3818">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3819">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3819">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3820">16</span><span class="sxs-lookup"><span data-stu-id="937fc-3820">16</span></span> |
| <span data-ttu-id="937fc-3821">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3821">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3823">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3823">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3825">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3825">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3827">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3827">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3828">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3828">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3829">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3829">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3831">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3831">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3833">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3833">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3835">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3835">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3837">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3837">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3839">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3839">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-3840">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3840">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3841">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3841">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3842">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3842">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-3843">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3843">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3844">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3844">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3846">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3846">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-3847">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3847">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3849">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3849">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3850">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3850">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3851">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3851">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3852">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3852">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3853">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3853">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3854">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3854">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3856">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3856">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3858">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3858">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3860">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3860">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3861">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3861">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3862">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3862">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3863">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3863">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-3864">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3864">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3865">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3865">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3866">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3866">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3868">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3868">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3870">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3870">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3872">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3872">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-3874">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3874">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-3875">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3875">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3877">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3877">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3878">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3878">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3880">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3880">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3881">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3881">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3882">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3882">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3883">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3883">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-3884">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3884">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3885">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3885">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="937fc-3887">DXGI_FORMAT_R16_TYPELESS<sup>PCs</sup> (53)</span><span class="sxs-lookup"><span data-stu-id="937fc-3887">DXGI_FORMAT_R16_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="937fc-3888">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3888">Target</span></span> | <span data-ttu-id="937fc-3889">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3889">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3890">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3891">16</span><span class="sxs-lookup"><span data-stu-id="937fc-3891">16</span></span> |
| <span data-ttu-id="937fc-3892">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3892">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3894">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3894">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3895">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3896">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3897">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3898">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3900">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3900">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3902">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3904">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3904">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3906">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3906">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-3907">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3907">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-3908">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3908">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3909">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3909">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3910">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3910">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-3911">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3911">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3912">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3912">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3914">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3914">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-3915">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3915">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3916">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3916">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3917">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3917">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3918">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3918">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3919">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3919">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3920">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3920">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3921">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3921">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-3922">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3922">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-3923">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3923">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-3924">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3924">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3925">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3925">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3926">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3926">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3927">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3927">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-3928">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-3928">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3929">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-3929">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-3930">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-3930">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3932">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3932">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3933">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3933">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-3934">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-3934">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-3935">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-3935">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-3936">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3936">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-3937">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-3937">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-3938">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-3938">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3940">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-3940">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-3941">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3941">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-3942">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-3942">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-3943">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3943">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3945">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-3945">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-3946">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-3946">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="937fc-3948">DXGI_FORMAT_R16_FLOAT<sup>(</sup> 54)</span><span class="sxs-lookup"><span data-stu-id="937fc-3948">DXGI_FORMAT_R16_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="937fc-3949">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3949">Target</span></span> | <span data-ttu-id="937fc-3950">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-3950">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-3951">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-3951">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-3952">16</span><span class="sxs-lookup"><span data-stu-id="937fc-3952">16</span></span> |
| <span data-ttu-id="937fc-3953">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-3953">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3955">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3955">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3957">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-3957">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3959">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-3959">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3960">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-3960">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-3961">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-3961">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3963">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-3963">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3965">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-3965">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3967">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-3967">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3969">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-3969">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3971">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3971">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3973">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3973">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-3974">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-3974">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-3975">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-3975">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3977">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-3977">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-3978">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3978">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3980">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-3980">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3982">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3982">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3984">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-3984">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3986">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-3986">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-3987">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-3987">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-3988">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3988">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3989">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-3989">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-3990">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-3990">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3992">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-3992">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3994">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-3994">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-3996">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-3996">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-3997">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-3997">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-3998">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-3998">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-3999">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-3999">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4000">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4000">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4001">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4001">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4002">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4002">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4004">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4004">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4006">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4006">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4008">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4008">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4010">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4010">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4012">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4012">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4014">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4014">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4015">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4015">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4017">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4017">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4018">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4018">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4019">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4019">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4020">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4020">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4022">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4022">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4023">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4023">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="937fc-4025">DXGI_FORMAT_D16_UNORM<sup>(</sup> 55)</span><span class="sxs-lookup"><span data-stu-id="937fc-4025">DXGI_FORMAT_D16_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="937fc-4026">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4026">Target</span></span> | <span data-ttu-id="937fc-4027">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4027">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4028">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4028">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4029">16</span><span class="sxs-lookup"><span data-stu-id="937fc-4029">16</span></span> |
| <span data-ttu-id="937fc-4030">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4030">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4032">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4032">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4033">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4033">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4034">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4034">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4035">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4035">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4036">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4036">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4038">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4038">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4040">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4040">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-4041">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4041">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4043">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4043">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-4044">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4044">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-4045">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4045">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4046">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4046">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4047">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4047">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-4048">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4048">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4049">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4049">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4051">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4051">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-4052">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4052">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4053">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4053">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4054">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4054">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-4055">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4055">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4057">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4057">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4058">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4058">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4059">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4059">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-4060">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4060">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-4061">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4061">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-4062">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4062">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4063">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4063">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4064">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4064">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4065">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4065">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4066">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4066">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4067">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4067">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4068">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4068">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4070">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4070">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4072">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4072">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4074">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4074">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4076">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4076">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-4077">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4077">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-4078">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4078">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4079">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4079">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4081">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4081">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4082">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4082">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4083">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4083">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4084">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4084">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4086">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4086">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4087">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4087">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="937fc-4089">DXGI_FORMAT_R16_UNORM<sup>(</sup> 56)</span><span class="sxs-lookup"><span data-stu-id="937fc-4089">DXGI_FORMAT_R16_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="937fc-4090">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4090">Target</span></span> | <span data-ttu-id="937fc-4091">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4091">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4092">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4093">16</span><span class="sxs-lookup"><span data-stu-id="937fc-4093">16</span></span> |
| <span data-ttu-id="937fc-4094">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4094">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4096">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4096">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4098">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4098">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4100">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4100">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4101">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4101">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4102">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4102">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4104">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4106">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4108">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4108">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4110">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4110">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4112">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4112">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4114">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4114">Shader sample_c (comparison filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4116">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4116">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4117">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4117">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4119">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4119">Shader gather4_c</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4121">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4121">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4123">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4123">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4125">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4125">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4127">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4127">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4129">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4129">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-4130">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4130">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4131">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4131">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4132">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4132">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4133">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4133">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4135">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4135">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4137">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4137">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4139">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4139">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4140">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4140">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4141">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4141">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4142">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4142">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4143">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4143">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4144">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4144">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4145">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4145">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4147">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4147">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4149">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4149">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4151">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4151">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4153">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4153">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4155">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4155">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4157">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4157">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4158">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4158">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4160">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4160">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4161">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4161">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4162">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4162">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4163">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4163">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4165">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4165">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4166">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4166">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="937fc-4168">DXGI_FORMAT_R16_UINT<sup>(</sup> 57)</span><span class="sxs-lookup"><span data-stu-id="937fc-4168">DXGI_FORMAT_R16_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="937fc-4169">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4169">Target</span></span> | <span data-ttu-id="937fc-4170">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4170">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4171">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4171">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4172">16</span><span class="sxs-lookup"><span data-stu-id="937fc-4172">16</span></span> |
| <span data-ttu-id="937fc-4173">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4173">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4175">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4175">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4177">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4177">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4179">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4179">Input Assembler Index Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4181">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4181">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4182">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4182">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4184">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4184">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4186">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4186">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4188">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4188">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4190">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4190">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4192">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4192">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-4193">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4193">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4194">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4194">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4195">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4195">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-4196">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4196">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4197">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4197">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4199">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4199">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-4200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4200">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4202">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4202">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4203">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4203">Output Merger Logic Op</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4205">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4206">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4207">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4208">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4208">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4210">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4210">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4212">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4212">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4214">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4215">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4216">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4216">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4217">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4218">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4218">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4219">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4219">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4220">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4220">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4222">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4222">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4224">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4224">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4226">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4226">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4228">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4228">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-4229">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4229">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4231">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4231">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4232">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4232">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4234">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4235">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4236">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4237">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4237">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4239">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4239">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4240">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4240">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="937fc-4242">DXGI_FORMAT_R16_SNORM<sup>(</sup> 58)</span><span class="sxs-lookup"><span data-stu-id="937fc-4242">DXGI_FORMAT_R16_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="937fc-4243">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4243">Target</span></span> | <span data-ttu-id="937fc-4244">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4244">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4245">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4245">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4246">16</span><span class="sxs-lookup"><span data-stu-id="937fc-4246">16</span></span> |
| <span data-ttu-id="937fc-4247">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4247">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4249">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4249">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4251">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4251">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4253">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4253">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4254">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4254">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4255">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4255">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4257">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4259">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4259">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4261">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4261">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4263">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4263">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4265">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4265">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4267">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4267">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4268">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4268">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4269">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4269">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4271">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4271">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4272">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4272">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4274">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4274">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4276">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4276">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4278">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4278">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4280">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4280">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-4281">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4281">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4282">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4282">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4283">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4283">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4284">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4284">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4286">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4286">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4288">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4288">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4290">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4290">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4291">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4291">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4292">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4292">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4293">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4293">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4294">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4294">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4295">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4295">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4296">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4296">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4298">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4298">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4300">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4300">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4302">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4302">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4304">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4304">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4306">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4306">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4308">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4308">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4309">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4309">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4311">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4311">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4312">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4312">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4313">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4313">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4314">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4314">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4316">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4316">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4317">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4317">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="937fc-4319">DXGI_FORMAT_R16_SINT<sup>(</sup> 59)</span><span class="sxs-lookup"><span data-stu-id="937fc-4319">DXGI_FORMAT_R16_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="937fc-4320">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4320">Target</span></span> | <span data-ttu-id="937fc-4321">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4321">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4322">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4322">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4323">16</span><span class="sxs-lookup"><span data-stu-id="937fc-4323">16</span></span> |
| <span data-ttu-id="937fc-4324">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4324">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4326">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4326">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4328">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4328">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4330">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4330">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4331">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4331">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4332">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4332">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4334">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4336">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4336">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4338">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4338">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4340">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4340">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4342">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4342">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-4343">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4343">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4344">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4344">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4345">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4345">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-4346">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4346">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4347">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4347">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4349">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4349">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-4350">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4350">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4352">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4352">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4353">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4353">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-4354">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4354">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4355">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4355">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4356">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4356">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4357">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4357">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4359">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4359">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4361">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4361">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4363">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4363">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4364">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4364">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4365">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4365">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4366">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4366">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4367">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4367">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4368">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4368">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4369">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4369">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4371">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4371">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4373">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4373">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4375">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4375">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4377">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-4378">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4378">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4380">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4380">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4381">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4381">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4383">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4383">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4384">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4384">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4385">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4385">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4386">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4386">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4388">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4388">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4389">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4389">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="937fc-4391">DXGI_FORMAT_R8_TYPELESS<sup>PCs</sup> (60)</span><span class="sxs-lookup"><span data-stu-id="937fc-4391">DXGI_FORMAT_R8_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="937fc-4392">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4392">Target</span></span> | <span data-ttu-id="937fc-4393">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4393">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4394">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4394">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4395">8</span><span class="sxs-lookup"><span data-stu-id="937fc-4395">8</span></span> |
| <span data-ttu-id="937fc-4396">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4396">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4398">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4398">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4399">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4399">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4400">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4400">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4401">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4401">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4402">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4402">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4404">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4406">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4406">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4408">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4408">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4410">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4410">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-4411">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4411">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-4412">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4412">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4413">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4413">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4414">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4414">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-4415">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4415">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4416">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4416">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4418">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4418">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-4419">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4419">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4420">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4420">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4421">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4421">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-4422">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4422">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4423">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4423">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4424">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4424">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4425">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4425">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-4426">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4426">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-4427">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4427">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-4428">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4428">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4429">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4429">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4430">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4430">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4431">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4431">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4432">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4432">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4433">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4433">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4434">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4434">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4436">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4437">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4438">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-4439">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-4440">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4440">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-4441">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4442">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4442">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4444">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4444">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4445">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4445">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4446">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4446">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4447">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4447">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4449">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4449">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4450">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4450">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="937fc-4452">DXGI_FORMAT_R8_UNORM<sup>(</sup> 61)</span><span class="sxs-lookup"><span data-stu-id="937fc-4452">DXGI_FORMAT_R8_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="937fc-4453">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4453">Target</span></span> | <span data-ttu-id="937fc-4454">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4454">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4455">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4455">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4456">8</span><span class="sxs-lookup"><span data-stu-id="937fc-4456">8</span></span> |
| <span data-ttu-id="937fc-4457">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4457">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4459">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4459">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4461">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4461">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4463">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4463">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4464">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4464">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4465">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4465">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4467">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4467">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4469">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4469">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4471">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4471">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4473">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4473">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4475">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4475">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4477">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4477">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4478">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4478">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4479">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4479">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4481">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4481">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4482">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4482">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4484">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4484">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4486">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4486">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4488">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4488">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4490">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4490">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-4491">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4491">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4492">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4492">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4493">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4493">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4494">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4494">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4496">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4496">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4498">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4498">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4500">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4500">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4501">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4501">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4502">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4502">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4503">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4503">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4504">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4504">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4505">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4505">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4506">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4506">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4508">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4508">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4510">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4510">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4512">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4512">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4514">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4514">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4516">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4516">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4518">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4518">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4519">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4519">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4521">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4521">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4522">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4522">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4523">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4523">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4524">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4524">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4526">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4526">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4527">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4527">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="937fc-4529">DXGI_FORMAT_R8_UINT<sup>(</sup> 62)</span><span class="sxs-lookup"><span data-stu-id="937fc-4529">DXGI_FORMAT_R8_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="937fc-4530">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4530">Target</span></span> | <span data-ttu-id="937fc-4531">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4531">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4532">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4532">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4533">8</span><span class="sxs-lookup"><span data-stu-id="937fc-4533">8</span></span> |
| <span data-ttu-id="937fc-4534">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4534">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4536">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4536">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4538">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4538">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4540">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4540">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4541">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4541">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4542">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4542">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4544">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4544">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4546">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4546">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4548">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4548">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4550">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4550">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4552">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4552">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-4553">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4553">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4554">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4554">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4555">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4555">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-4556">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4556">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4557">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4557">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4559">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4559">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-4560">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4560">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4562">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4562">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4563">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4563">Output Merger Logic Op</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4565">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4566">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4567">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4568">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4568">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4570">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4570">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4572">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4572">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4574">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4575">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4576">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4577">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4578">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4578">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4579">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4579">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4580">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4580">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4582">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4582">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4584">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4584">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4586">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4586">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4588">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4588">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-4589">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4589">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4591">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4591">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4592">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4592">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4594">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4594">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4595">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4595">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4596">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4596">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4597">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4597">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4599">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4599">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4600">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4600">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="937fc-4602">DXGI_FORMAT_R8_SNORM<sup>(</sup> 63)</span><span class="sxs-lookup"><span data-stu-id="937fc-4602">DXGI_FORMAT_R8_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="937fc-4603">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4603">Target</span></span> | <span data-ttu-id="937fc-4604">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4604">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4605">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4605">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4606">8</span><span class="sxs-lookup"><span data-stu-id="937fc-4606">8</span></span> |
| <span data-ttu-id="937fc-4607">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4607">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4609">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4609">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4611">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4611">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4613">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4613">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4614">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4614">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4615">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4615">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4617">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4617">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4619">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4619">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4621">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4621">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4623">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4623">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4625">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4625">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4627">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4627">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4628">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4628">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4629">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4629">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4631">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4631">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4632">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4632">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4634">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4634">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4636">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4636">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4638">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4638">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4640">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4640">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-4641">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4641">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4642">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4642">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4643">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4643">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4644">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4644">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4646">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4646">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4648">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4648">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4650">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4650">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4651">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4651">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4652">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4652">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4653">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4653">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4654">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4654">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4655">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4655">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4656">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4656">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4658">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4658">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4660">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4660">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4662">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4662">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4664">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4664">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4666">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4666">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4668">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4668">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4669">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4669">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4671">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4671">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4672">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4672">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4673">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4673">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4674">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4674">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4676">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4676">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4677">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4677">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="937fc-4679">DXGI_FORMAT_R8_SINT<sup>(</sup> 64)</span><span class="sxs-lookup"><span data-stu-id="937fc-4679">DXGI_FORMAT_R8_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="937fc-4680">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4680">Target</span></span> | <span data-ttu-id="937fc-4681">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4681">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4682">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4682">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4683">8</span><span class="sxs-lookup"><span data-stu-id="937fc-4683">8</span></span> |
| <span data-ttu-id="937fc-4684">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4684">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4686">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4686">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4688">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4688">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4690">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4690">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4691">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4691">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4692">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4692">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4694">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4696">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4696">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4698">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4698">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4700">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4700">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4702">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4702">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-4703">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4703">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4704">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4704">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4705">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4705">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-4706">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4706">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4707">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4707">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4709">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4709">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-4710">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4710">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4712">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4712">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4713">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4713">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-4714">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4714">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4715">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4715">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4716">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4716">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4717">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4717">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4719">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4719">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4721">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4721">UAV Typed Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4723">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4723">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4724">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4724">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4725">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4725">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4726">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4726">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4727">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4727">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4728">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4728">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4729">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4729">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4731">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4731">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4733">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4733">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4735">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4735">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4737">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4737">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-4738">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4738">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4740">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4740">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4741">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4741">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4743">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4743">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4744">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4744">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4745">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4745">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4746">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4746">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4748">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4748">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4749">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4749">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="937fc-4751">DXGI_FORMAT_A8_UNORM<sup>(</sup> 65)</span><span class="sxs-lookup"><span data-stu-id="937fc-4751">DXGI_FORMAT_A8_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="937fc-4752">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4752">Target</span></span> | <span data-ttu-id="937fc-4753">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4753">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4754">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4754">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4755">8</span><span class="sxs-lookup"><span data-stu-id="937fc-4755">8</span></span> |
| <span data-ttu-id="937fc-4756">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4756">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4758">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4758">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4759">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4759">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4760">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4760">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4761">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4761">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4762">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4762">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4764">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4764">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4766">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4766">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4768">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4768">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4770">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4770">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4772">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4772">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4774">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4774">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4775">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4775">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4776">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4776">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4778">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4778">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4779">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4779">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4781">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4781">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4783">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4785">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4785">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4787">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4787">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-4788">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4788">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4789">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4789">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4790">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4790">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4791">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4791">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4793">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4793">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4795">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4795">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4797">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4797">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4798">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4798">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4799">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4799">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4800">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4800">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4801">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4801">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4802">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4802">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4803">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4803">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4805">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4805">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4807">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4807">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4809">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4809">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-4811">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4811">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4813">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4813">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4815">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4815">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4816">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4816">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-4817">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4817">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4818">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4818">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4819">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4819">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4820">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4820">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4822">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4822">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4823">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4823">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="937fc-4825">DXGI_FORMAT_R9G9B9E5_SHAREDEXP von "<sup>f</sup> " (67)</span><span class="sxs-lookup"><span data-stu-id="937fc-4825">DXGI_FORMAT_R9G9B9E5_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="937fc-4826">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4826">Target</span></span> | <span data-ttu-id="937fc-4827">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4827">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4828">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4828">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4829">32</span><span class="sxs-lookup"><span data-stu-id="937fc-4829">32</span></span> |
| <span data-ttu-id="937fc-4830">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4830">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4832">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4832">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4833">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4833">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4834">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4834">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4835">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4835">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4836">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4836">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4838">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4838">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4840">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4840">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4842">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4842">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4844">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4844">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4846">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4846">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4848">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4848">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4849">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4849">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4850">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4850">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4852">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4852">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4853">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4853">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4855">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4855">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-4856">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4856">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4857">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4857">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4858">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4858">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-4859">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4859">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4860">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4860">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4861">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4861">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4862">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4862">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-4863">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4863">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-4864">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4864">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-4865">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4865">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4866">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4866">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4867">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4867">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4868">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4868">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4869">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4869">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4870">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4870">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4871">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4871">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4873">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4873">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4874">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4874">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4875">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4875">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-4876">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4876">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-4877">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4877">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-4878">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4878">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4879">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4879">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-4880">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4880">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4881">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4881">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4882">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4882">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4883">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4883">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-4884">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4884">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4885">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4885">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="937fc-4887">DXGI_FORMAT_R8G8_B8G8_UNORM von "<sup>f</sup> " (68)</span><span class="sxs-lookup"><span data-stu-id="937fc-4887">DXGI_FORMAT_R8G8_B8G8_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="937fc-4888">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4888">Target</span></span> | <span data-ttu-id="937fc-4889">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4889">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4890">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4891">16</span><span class="sxs-lookup"><span data-stu-id="937fc-4891">16</span></span> |
| <span data-ttu-id="937fc-4892">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4892">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4894">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4894">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4895">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4896">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4897">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4898">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4900">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4900">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4902">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4904">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4904">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4906">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4906">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4908">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4908">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4910">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4910">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4911">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4911">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4912">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4912">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4914">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4914">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4915">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4915">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4917">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4917">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-4918">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4918">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4919">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4919">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4920">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4920">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-4921">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4921">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4922">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4922">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4923">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4923">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4924">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4924">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-4925">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4925">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-4926">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4926">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-4927">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4927">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4928">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4928">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4929">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4929">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4930">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4930">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4931">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4931">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4932">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4932">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4933">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4933">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4935">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4935">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4936">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4936">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4937">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4937">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-4938">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4938">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-4939">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4939">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-4940">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-4940">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-4941">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-4941">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-4942">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-4942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-4943">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-4944">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-4944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-4945">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4945">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-4946">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-4946">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-4947">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-4947">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="937fc-4948">DXGI_FORMAT_G8R8_G8B8_UNORM von "<sup>f</sup> " (69)</span><span class="sxs-lookup"><span data-stu-id="937fc-4948">DXGI_FORMAT_G8R8_G8B8_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="937fc-4949">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4949">Target</span></span> | <span data-ttu-id="937fc-4950">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-4950">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-4951">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-4951">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-4952">16</span><span class="sxs-lookup"><span data-stu-id="937fc-4952">16</span></span> |
| <span data-ttu-id="937fc-4953">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-4953">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4955">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4955">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4956">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-4956">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4957">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-4957">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4958">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-4958">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-4959">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-4959">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4961">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-4961">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4963">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-4963">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4965">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-4965">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4967">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-4967">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4969">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4969">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4971">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4971">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-4972">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-4972">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-4973">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-4973">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4975">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-4975">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-4976">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4976">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4978">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-4978">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-4979">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4979">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4980">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4980">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4981">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-4981">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-4982">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-4982">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-4983">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4983">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4984">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-4984">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-4985">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-4985">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-4986">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-4986">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-4987">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-4987">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-4988">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-4988">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-4989">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-4989">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-4990">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-4990">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-4991">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-4991">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-4992">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-4992">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4993">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-4993">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-4994">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-4994">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-4996">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4996">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4997">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-4997">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-4998">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-4998">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-4999">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-4999">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5000">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5000">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5001">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5001">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5002">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5002">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-5003">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5003">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5004">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5004">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5005">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5005">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5006">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5006">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-5007">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5007">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5008">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5008">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="937fc-5009">DXGI_FORMAT_BC1_TYPELESS<sup>PCC</sup> (70)</span><span class="sxs-lookup"><span data-stu-id="937fc-5009">DXGI_FORMAT_BC1_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="937fc-5010">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5010">Target</span></span> | <span data-ttu-id="937fc-5011">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5011">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5012">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5012">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5013">64</span><span class="sxs-lookup"><span data-stu-id="937fc-5013">64</span></span> |
| <span data-ttu-id="937fc-5014">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5014">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5016">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5016">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5017">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5017">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5018">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5018">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5019">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5019">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5020">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5020">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5021">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5023">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5025">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5027">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5027">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-5028">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5028">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-5029">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5029">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5030">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5030">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5031">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5031">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-5032">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5032">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5033">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5033">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5035">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5035">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5036">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5036">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5037">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5037">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5038">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5038">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5039">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5039">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5040">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5040">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5041">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5041">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5042">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5042">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5043">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5043">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5044">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5044">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5045">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5045">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5046">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5046">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5047">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5047">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5048">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5048">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5049">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5049">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5050">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5050">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5051">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5051">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5053">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5053">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5054">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5054">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5055">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5055">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5056">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5056">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5057">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5057">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5058">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5058">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5059">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5059">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5061">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5061">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5062">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5062">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5063">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5063">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5064">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5064">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5066">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5066">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5067">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5067">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a><span data-ttu-id="937fc-5069">DXGI_FORMAT_BC1_UNORM <sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="937fc-5069">DXGI_FORMAT_BC1_UNORM <sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="937fc-5070">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5070">Target</span></span> | <span data-ttu-id="937fc-5071">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5071">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5072">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5072">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5073">64</span><span class="sxs-lookup"><span data-stu-id="937fc-5073">64</span></span> |
| <span data-ttu-id="937fc-5074">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5074">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5076">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5076">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5077">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5077">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5078">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5078">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5079">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5079">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5080">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5080">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5081">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5081">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5083">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5083">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5085">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5085">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5087">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5087">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5089">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5089">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5091">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5091">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5092">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5092">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5093">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5093">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5095">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5095">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5096">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5096">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5098">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5098">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5099">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5099">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5100">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5101">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5102">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5103">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5104">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5105">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5105">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5106">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5107">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5108">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5109">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5110">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5111">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5112">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5112">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5113">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5113">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5114">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5114">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5116">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5116">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5117">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5117">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5118">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5118">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5119">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5119">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5120">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5120">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5121">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5121">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5122">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5122">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5124">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5124">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5125">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5125">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5126">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5126">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5127">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5127">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5129">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5129">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5130">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5130">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a><span data-ttu-id="937fc-5132">DXGI_FORMAT_BC1_UNORM_SRGB <sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="937fc-5132">DXGI_FORMAT_BC1_UNORM_SRGB <sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="937fc-5133">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5133">Target</span></span> | <span data-ttu-id="937fc-5134">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5134">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5135">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5135">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5136">64</span><span class="sxs-lookup"><span data-stu-id="937fc-5136">64</span></span> |
| <span data-ttu-id="937fc-5137">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5137">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5139">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5139">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5140">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5140">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5141">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5141">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5142">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5142">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5143">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5143">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5144">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5146">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5148">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5148">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5150">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5150">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5152">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5152">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5154">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5154">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5155">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5155">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5156">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5156">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5158">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5158">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5159">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5159">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5161">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5161">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5162">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5162">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5163">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5163">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5164">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5164">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5165">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5165">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5166">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5166">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5167">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5167">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5168">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5168">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5169">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5169">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5170">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5170">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5171">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5171">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5172">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5172">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5173">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5173">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5174">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5174">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5175">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5175">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5176">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5176">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5177">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5177">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5179">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5179">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5180">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5180">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5181">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5181">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5182">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5182">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5183">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5183">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5184">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5184">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5185">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5185">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5187">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5187">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5188">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5188">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5189">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5189">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5190">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5190">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5192">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5192">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5193">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5193">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="937fc-5195">DXGI_FORMAT_BC2_TYPELESS<sup>PCC</sup> (73)</span><span class="sxs-lookup"><span data-stu-id="937fc-5195">DXGI_FORMAT_BC2_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="937fc-5196">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5196">Target</span></span> | <span data-ttu-id="937fc-5197">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5197">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5198">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5198">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5199">128</span><span class="sxs-lookup"><span data-stu-id="937fc-5199">128</span></span> |
| <span data-ttu-id="937fc-5200">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5200">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5202">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5202">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5203">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5204">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5205">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5206">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5207">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5209">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5209">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5211">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5211">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5213">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5213">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-5214">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5214">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-5215">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5215">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5216">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5216">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5217">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5217">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-5218">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5218">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5219">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5219">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5221">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5221">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5222">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5222">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5223">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5223">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5224">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5224">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5225">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5225">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5226">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5226">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5227">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5227">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5228">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5228">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5229">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5229">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5230">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5230">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5231">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5231">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5232">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5232">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5233">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5233">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5234">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5234">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5235">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5235">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5236">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5236">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5237">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5237">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5239">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5239">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5240">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5240">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5241">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5241">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5242">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5242">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5243">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5243">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5244">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5244">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5245">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5245">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5247">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5247">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5248">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5248">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5249">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5249">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5250">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5250">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5252">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5252">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5253">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5253">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a><span data-ttu-id="937fc-5255">DXGI_FORMAT_BC2_UNORM <sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="937fc-5255">DXGI_FORMAT_BC2_UNORM <sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="937fc-5256">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5256">Target</span></span> | <span data-ttu-id="937fc-5257">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5257">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5258">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5258">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5259">128</span><span class="sxs-lookup"><span data-stu-id="937fc-5259">128</span></span> |
| <span data-ttu-id="937fc-5260">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5260">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5262">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5262">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5263">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5263">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5264">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5264">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5265">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5265">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5266">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5266">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5267">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5269">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5271">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5271">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5273">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5273">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5275">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5275">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5277">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5277">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5278">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5278">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5279">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5279">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5281">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5281">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5282">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5282">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5284">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5284">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5285">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5285">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5286">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5286">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5287">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5287">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5288">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5288">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5289">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5289">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5290">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5290">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5291">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5291">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5292">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5292">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5293">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5293">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5294">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5294">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5295">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5295">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5296">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5296">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5297">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5297">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5298">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5298">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5299">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5299">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5300">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5300">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5302">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5302">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5303">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5303">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5304">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5304">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5305">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5305">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5306">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5306">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5307">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5307">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5308">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5308">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5310">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5310">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5311">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5311">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5312">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5312">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5313">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5313">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5315">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5315">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5316">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5316">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a><span data-ttu-id="937fc-5318">DXGI_FORMAT_BC2_UNORM_SRGB <sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="937fc-5318">DXGI_FORMAT_BC2_UNORM_SRGB <sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="937fc-5319">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5319">Target</span></span> | <span data-ttu-id="937fc-5320">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5320">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5321">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5321">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5322">128</span><span class="sxs-lookup"><span data-stu-id="937fc-5322">128</span></span> |
| <span data-ttu-id="937fc-5323">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5323">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5325">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5325">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5326">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5326">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5327">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5327">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5328">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5328">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5329">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5329">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5330">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5330">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5332">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5332">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5334">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5334">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5336">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5336">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5338">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5338">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5340">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5340">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5341">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5341">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5342">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5342">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5344">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5344">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5345">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5345">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5347">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5347">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5348">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5348">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5349">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5349">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5350">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5350">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5351">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5351">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5352">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5352">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5353">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5353">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5354">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5354">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5355">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5355">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5356">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5356">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5357">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5357">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5358">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5358">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5359">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5359">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5360">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5360">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5361">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5361">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5362">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5362">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5363">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5363">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5365">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5365">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5366">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5366">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5367">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5367">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5368">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5369">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5369">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5370">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5370">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5371">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5371">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5373">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5373">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5374">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5374">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5375">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5375">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5376">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5376">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5378">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5378">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5379">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5379">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="937fc-5381">DXGI_FORMAT_BC3_TYPELESS<sup>PCC</sup> (76)</span><span class="sxs-lookup"><span data-stu-id="937fc-5381">DXGI_FORMAT_BC3_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="937fc-5382">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5382">Target</span></span> | <span data-ttu-id="937fc-5383">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5383">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5384">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5384">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5385">128</span><span class="sxs-lookup"><span data-stu-id="937fc-5385">128</span></span> |
| <span data-ttu-id="937fc-5386">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5386">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5388">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5388">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5389">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5389">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5390">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5390">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5391">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5391">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5392">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5392">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5393">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5393">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5395">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5395">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5397">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5397">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5399">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5399">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-5400">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-5401">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5401">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5402">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5402">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5403">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5403">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-5404">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5404">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5405">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5405">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5407">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5407">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5408">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5408">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5409">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5409">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5410">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5410">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5411">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5411">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5412">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5412">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5413">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5413">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5414">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5414">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5415">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5415">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5416">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5416">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5417">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5417">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5418">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5418">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5419">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5419">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5420">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5420">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5421">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5421">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5422">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5422">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5423">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5423">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5425">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5426">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5427">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5428">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5429">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5429">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5430">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5431">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5431">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5433">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5433">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5434">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5434">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5435">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5435">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5436">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5436">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5438">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5438">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5439">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5439">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a><span data-ttu-id="937fc-5441">DXGI_FORMAT_BC3_UNORM <sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="937fc-5441">DXGI_FORMAT_BC3_UNORM <sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="937fc-5442">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5442">Target</span></span> | <span data-ttu-id="937fc-5443">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5443">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5444">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5444">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5445">128</span><span class="sxs-lookup"><span data-stu-id="937fc-5445">128</span></span> |
| <span data-ttu-id="937fc-5446">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5446">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5448">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5448">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5449">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5449">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5450">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5450">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5451">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5451">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5452">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5452">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5453">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5453">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5455">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5457">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5457">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5459">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5459">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5461">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5461">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5463">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5463">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5464">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5464">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5465">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5465">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5467">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5467">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5468">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5468">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5470">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5470">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5471">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5471">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5472">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5472">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5473">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5473">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5474">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5474">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5475">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5475">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5476">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5476">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5477">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5477">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5478">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5478">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5479">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5479">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5480">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5480">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5481">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5481">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5482">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5482">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5483">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5483">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5484">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5484">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5485">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5485">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5486">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5486">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5488">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5488">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5489">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5489">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5490">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5490">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5491">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5491">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5492">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5492">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5493">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5493">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5494">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5494">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5496">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5496">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5497">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5497">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5498">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5498">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5499">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5499">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5501">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5501">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5502">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5502">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a><span data-ttu-id="937fc-5504">DXGI_FORMAT_BC3_UNORM_SRGB <sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="937fc-5504">DXGI_FORMAT_BC3_UNORM_SRGB <sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="937fc-5505">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5505">Target</span></span> | <span data-ttu-id="937fc-5506">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5506">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5507">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5507">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5508">128</span><span class="sxs-lookup"><span data-stu-id="937fc-5508">128</span></span> |
| <span data-ttu-id="937fc-5509">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5509">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5511">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5511">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5512">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5512">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5513">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5513">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5514">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5514">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5515">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5515">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5516">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5518">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5520">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5522">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5522">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5524">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5524">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5526">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5526">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5527">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5527">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5528">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5528">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5530">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5530">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5531">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5531">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5533">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5533">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5534">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5535">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5535">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5536">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5536">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5537">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5537">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5538">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5538">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5539">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5539">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5540">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5540">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5541">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5541">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5542">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5542">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5543">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5543">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5544">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5544">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5545">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5545">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5546">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5546">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5547">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5547">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5548">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5548">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5549">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5549">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5551">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5551">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5552">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5552">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5553">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5553">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5554">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5554">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5555">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5555">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5556">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5556">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5557">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5557">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5559">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5559">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5560">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5560">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5561">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5561">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5562">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5562">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5564">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5564">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5565">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5565">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="937fc-5567">DXGI_FORMAT_BC4_TYPELESS<sup>PCC</sup> (79)</span><span class="sxs-lookup"><span data-stu-id="937fc-5567">DXGI_FORMAT_BC4_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="937fc-5568">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5568">Target</span></span> | <span data-ttu-id="937fc-5569">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5569">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5570">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5570">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5571">64</span><span class="sxs-lookup"><span data-stu-id="937fc-5571">64</span></span> |
| <span data-ttu-id="937fc-5572">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5572">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5574">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5574">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5575">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5575">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5576">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5576">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5577">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5577">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5578">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5578">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5579">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5579">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5581">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5581">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5583">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5583">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5585">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5585">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-5586">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5586">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-5587">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5587">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5588">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5588">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5589">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5589">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-5590">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5590">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5591">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5591">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5593">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5593">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5594">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5594">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5595">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5595">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5596">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5596">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5597">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5597">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5598">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5598">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5599">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5599">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5600">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5600">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5601">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5601">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5602">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5602">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5603">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5603">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5604">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5604">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5605">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5605">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5606">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5606">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5607">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5607">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5608">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5608">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5609">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5609">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5611">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5611">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5612">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5612">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5613">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5613">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5614">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5614">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5615">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5615">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5616">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5616">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5617">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5617">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5619">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5619">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5620">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5620">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5621">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5621">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5622">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5622">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-5623">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5623">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5624">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5624">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a><span data-ttu-id="937fc-5626">DXGI_FORMAT_BC4_UNORM <sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="937fc-5626">DXGI_FORMAT_BC4_UNORM <sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="937fc-5627">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5627">Target</span></span> | <span data-ttu-id="937fc-5628">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5628">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5629">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5629">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5630">64</span><span class="sxs-lookup"><span data-stu-id="937fc-5630">64</span></span> |
| <span data-ttu-id="937fc-5631">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5631">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5633">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5633">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5634">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5634">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5635">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5635">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5636">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5636">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5637">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5637">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5638">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5638">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5640">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5640">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5642">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5642">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5644">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5644">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5646">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5646">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5648">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5648">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5649">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5649">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5650">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5650">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5652">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5652">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5653">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5653">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5655">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5655">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5656">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5656">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5657">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5657">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5658">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5658">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5659">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5659">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5660">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5660">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5661">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5661">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5662">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5662">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5663">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5663">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5664">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5664">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5665">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5665">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5666">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5666">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5667">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5667">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5668">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5668">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5669">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5669">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5670">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5670">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5671">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5671">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5673">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5673">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5674">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5674">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5675">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5675">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5676">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5676">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5677">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5677">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5678">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5678">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5679">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5679">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5681">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5681">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5682">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5682">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5683">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5683">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5684">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5684">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-5685">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5685">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5686">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5686">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a><span data-ttu-id="937fc-5688">DXGI_FORMAT_BC4_SNORM <sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="937fc-5688">DXGI_FORMAT_BC4_SNORM <sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="937fc-5689">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5689">Target</span></span> | <span data-ttu-id="937fc-5690">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5690">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5691">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5691">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5692">64</span><span class="sxs-lookup"><span data-stu-id="937fc-5692">64</span></span> |
| <span data-ttu-id="937fc-5693">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5693">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5695">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5695">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5696">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5696">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5697">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5697">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5698">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5698">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5699">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5699">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5700">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5700">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5702">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5702">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5704">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5704">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5706">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5706">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5708">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5708">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5710">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5710">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5711">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5711">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5712">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5712">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5714">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5714">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5715">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5715">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5717">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5717">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5718">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5718">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5719">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5719">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5720">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5720">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5721">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5721">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5722">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5722">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5723">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5723">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5724">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5724">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5725">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5725">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5726">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5726">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5727">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5727">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5728">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5728">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5729">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5729">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5730">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5730">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5731">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5731">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5732">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5732">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5733">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5733">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5735">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5735">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5736">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5736">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5737">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5737">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5738">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5738">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5739">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5739">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5740">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5740">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5741">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5741">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5743">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5743">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5744">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5744">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5745">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5745">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5746">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5746">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-5747">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5747">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5748">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5748">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="937fc-5750">DXGI_FORMAT_BC5_TYPELESS<sup>PCC</sup> (82)</span><span class="sxs-lookup"><span data-stu-id="937fc-5750">DXGI_FORMAT_BC5_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="937fc-5751">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5751">Target</span></span> | <span data-ttu-id="937fc-5752">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5752">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5753">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5753">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5754">128</span><span class="sxs-lookup"><span data-stu-id="937fc-5754">128</span></span> |
| <span data-ttu-id="937fc-5755">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5755">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5757">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5757">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5758">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5758">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5759">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5760">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5761">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5762">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5762">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5764">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5764">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5766">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5766">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5768">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5768">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-5769">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5769">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-5770">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5770">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5771">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5771">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5772">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5772">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-5773">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5773">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5774">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5774">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5776">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5776">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5777">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5777">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5778">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5778">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5779">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5779">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5780">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5780">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5781">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5781">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5782">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5782">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5783">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5783">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5784">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5784">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5785">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5785">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5786">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5786">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5787">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5787">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5788">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5788">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5789">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5789">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5790">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5790">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5791">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5791">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5792">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5792">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5794">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5794">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5795">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5795">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5796">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5796">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5797">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5797">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5798">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5798">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5799">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5799">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5800">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5800">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5802">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5802">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5803">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5803">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5804">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5804">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5805">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5805">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-5806">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5806">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5807">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5807">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a><span data-ttu-id="937fc-5809">DXGI_FORMAT_BC5_UNORM <sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="937fc-5809">DXGI_FORMAT_BC5_UNORM <sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="937fc-5810">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5810">Target</span></span> | <span data-ttu-id="937fc-5811">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5811">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5812">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5812">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5813">128</span><span class="sxs-lookup"><span data-stu-id="937fc-5813">128</span></span> |
| <span data-ttu-id="937fc-5814">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5814">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5816">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5816">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5817">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5817">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5818">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5818">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5819">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5819">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5820">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5820">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5821">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5821">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5823">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5823">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5825">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5825">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5827">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5827">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5829">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5829">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5831">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5831">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5832">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5832">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5833">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5833">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5835">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5835">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5836">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5836">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5838">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5838">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5839">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5840">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5841">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5842">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5843">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5844">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5845">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5845">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5846">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5847">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5848">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5849">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5850">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5851">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5852">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5852">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5853">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5853">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5854">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5854">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5856">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5857">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5858">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5859">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5860">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5860">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5861">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5862">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5862">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5864">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5864">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5865">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5865">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5866">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5866">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5867">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5867">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-5868">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5868">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5869">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5869">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a><span data-ttu-id="937fc-5871">DXGI_FORMAT_BC5_SNORM <sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="937fc-5871">DXGI_FORMAT_BC5_SNORM <sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="937fc-5872">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5872">Target</span></span> | <span data-ttu-id="937fc-5873">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5873">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5874">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5874">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5875">128</span><span class="sxs-lookup"><span data-stu-id="937fc-5875">128</span></span> |
| <span data-ttu-id="937fc-5876">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5876">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5878">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5878">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5879">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5879">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5880">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5880">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5881">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5881">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5882">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5882">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-5883">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5883">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5885">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5885">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5887">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5887">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5889">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5889">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5891">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5891">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5893">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5893">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5894">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5894">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5895">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5895">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5897">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5897">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5898">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5898">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5900">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5900">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-5901">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5901">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5902">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5902">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5903">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5903">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5904">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5904">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5905">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5905">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5906">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5906">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5907">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5907">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-5908">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5908">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-5909">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5909">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-5910">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5910">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5911">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5911">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5912">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5912">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5913">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5913">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5914">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5914">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5915">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5915">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5916">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5916">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5918">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5918">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5919">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5919">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-5920">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5920">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-5921">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5921">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-5922">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5922">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-5923">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5923">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-5924">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-5924">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5926">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-5926">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-5927">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5927">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-5928">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-5928">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-5929">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5929">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-5930">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-5930">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-5931">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-5931">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="937fc-5933">DXGI_FORMAT_B5G6R5_UNORM<sup>(</sup> 85)</span><span class="sxs-lookup"><span data-stu-id="937fc-5933">DXGI_FORMAT_B5G6R5_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="937fc-5934">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5934">Target</span></span> | <span data-ttu-id="937fc-5935">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-5935">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-5936">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-5936">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-5937">16</span><span class="sxs-lookup"><span data-stu-id="937fc-5937">16</span></span> |
| <span data-ttu-id="937fc-5938">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-5938">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5940">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5940">Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-5942">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-5942">Input Assembler Vertex Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-5944">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-5944">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5945">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-5945">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-5946">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-5946">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5948">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-5948">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-5950">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-5952">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5954">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-5954">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5956">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5956">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5958">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5958">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-5959">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-5959">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-5960">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-5960">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5962">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-5962">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-5963">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5963">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5965">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-5965">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5967">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5969">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5969">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5971">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-5971">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-5972">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-5972">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-5973">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5973">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5974">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-5974">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-5975">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-5975">Typed UAV</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-5977">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-5977">UAV Typed Store</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-5979">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5979">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-5981">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-5981">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-5982">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-5982">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-5983">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-5983">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-5984">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-5984">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-5985">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-5985">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5986">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-5986">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-5987">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-5987">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5989">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5989">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5991">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-5991">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5993">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-5993">Other Multisample Count RT</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5995">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-5995">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5997">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-5997">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-5999">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-5999">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6000">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6000">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-6001">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6001">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6002">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6002">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-6003">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6003">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-6004">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6004">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-6005">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6005">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6006">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6006">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="937fc-6008">DXGI_FORMAT_B5G5R5A1_UNORM<sup>(</sup> 86)</span><span class="sxs-lookup"><span data-stu-id="937fc-6008">DXGI_FORMAT_B5G5R5A1_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="937fc-6009">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6009">Target</span></span> | <span data-ttu-id="937fc-6010">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6010">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6011">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6011">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6012">16</span><span class="sxs-lookup"><span data-stu-id="937fc-6012">16</span></span> |
| <span data-ttu-id="937fc-6013">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6013">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6015">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6015">Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6017">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6017">Input Assembler Vertex Buffer</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6019">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6019">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6020">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6020">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6021">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6021">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6023">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6023">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6025">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6025">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6027">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6027">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6029">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6029">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6031">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6031">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6033">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6033">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6034">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6034">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6035">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6035">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6037">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6037">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6038">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6038">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6040">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6040">Mipmap Auto- Generation</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6042">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6042">RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6044">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6044">Blendable RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6046">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6046">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6047">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6047">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6048">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6048">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6049">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6049">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6050">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6050">Typed UAV</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6052">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6052">UAV Typed Store</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6054">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6054">UAV Typed Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6056">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6057">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6058">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6059">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6060">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6060">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6061">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6061">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6062">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6062">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6064">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6064">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6066">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6066">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6068">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6068">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6070">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6070">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6072">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6072">Multisample Load</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6074">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6074">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6075">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6075">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-6076">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6076">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6077">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6077">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-6078">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6078">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-6079">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6079">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-6080">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6080">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6081">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6081">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="937fc-6083">DXGI_FORMAT_B8G8R8A8_TYPELESS<sup>PCs</sup> (90)</span><span class="sxs-lookup"><span data-stu-id="937fc-6083">DXGI_FORMAT_B8G8R8A8_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="937fc-6084">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6084">Target</span></span> | <span data-ttu-id="937fc-6085">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6085">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6086">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6086">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6087">32</span><span class="sxs-lookup"><span data-stu-id="937fc-6087">32</span></span> |
| <span data-ttu-id="937fc-6088">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6088">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6090">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6090">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6091">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6091">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6092">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6092">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6093">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6093">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6094">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6094">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6096">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6096">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6098">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6098">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6100">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6100">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6102">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6102">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-6103">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6103">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-6104">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6104">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6105">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6105">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6106">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6106">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-6107">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6107">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6108">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6108">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6110">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6110">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-6111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6111">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6112">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6113">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6114">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6115">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6116">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6117">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6117">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-6118">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-6119">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6120">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6121">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6122">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6123">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6124">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6124">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6125">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6125">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6126">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6126">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6128">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6128">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6129">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6129">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6130">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6130">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-6131">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6131">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-6132">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6132">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-6133">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6133">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6134">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6134">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6136">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6136">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6137">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6137">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-6138">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6138">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-6139">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6139">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6141">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6141">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6142">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6142">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="937fc-6144">DXGI_FORMAT_B8G8R8A8_UNORM<sup>(</sup> 87)</span><span class="sxs-lookup"><span data-stu-id="937fc-6144">DXGI_FORMAT_B8G8R8A8_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="937fc-6145">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6145">Target</span></span> | <span data-ttu-id="937fc-6146">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6146">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6147">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6148">32</span><span class="sxs-lookup"><span data-stu-id="937fc-6148">32</span></span> |
| <span data-ttu-id="937fc-6149">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6149">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6151">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6151">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6153">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6153">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6155">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6155">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6156">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6156">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6157">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6157">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6159">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6159">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6161">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6161">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6163">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6165">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6165">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6167">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6167">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6169">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6169">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6170">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6170">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6171">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6171">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6173">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6173">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6174">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6174">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6176">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6176">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6178">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6178">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6180">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6180">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6182">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6182">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6183">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6183">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6184">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6184">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6185">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6185">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6186">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6186">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-6187">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6187">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-6188">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6188">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6189">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6189">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6190">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6190">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6191">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6191">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6192">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6192">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6193">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6193">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6194">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6194">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6195">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6195">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6197">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6197">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6199">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6199">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6201">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6201">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6203">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6203">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6205">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6205">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6207">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6207">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6209">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6209">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6211">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6211">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6212">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6212">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6214">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6214">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6216">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6216">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6218">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6218">BackBuffer Castable Even Fully Typed</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6220">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6220">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="937fc-6222">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB<sup>(</sup> 91)</span><span class="sxs-lookup"><span data-stu-id="937fc-6222">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="937fc-6223">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6223">Target</span></span> | <span data-ttu-id="937fc-6224">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6224">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6225">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6225">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6226">32</span><span class="sxs-lookup"><span data-stu-id="937fc-6226">32</span></span> |
| <span data-ttu-id="937fc-6227">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6227">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6229">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6229">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6230">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6230">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6231">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6232">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6233">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6235">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6235">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6237">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6237">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6239">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6241">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6241">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6243">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6243">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6245">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6245">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6246">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6246">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6247">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6247">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6249">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6249">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6250">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6250">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6252">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6252">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6254">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6254">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6256">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6256">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6258">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6258">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6259">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6259">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6260">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6260">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6261">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6261">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6262">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6262">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-6263">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6263">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-6264">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6264">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6265">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6265">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6266">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6266">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6267">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6267">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6268">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6268">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6269">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6269">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6270">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6270">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6271">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6271">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6273">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6273">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6275">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6275">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6277">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6277">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6279">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6279">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6281">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6281">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6283">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6283">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6285">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6285">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6287">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6287">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6288">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6288">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6290">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6290">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6292">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6292">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6294">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6294">BackBuffer Castable Even Fully Typed</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6296">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6296">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="937fc-6298">DXGI_FORMAT_B8G8R8X8_TYPELESS<sup>PCs</sup> (92)</span><span class="sxs-lookup"><span data-stu-id="937fc-6298">DXGI_FORMAT_B8G8R8X8_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="937fc-6299">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6299">Target</span></span> | <span data-ttu-id="937fc-6300">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6300">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6301">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6301">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6302">32</span><span class="sxs-lookup"><span data-stu-id="937fc-6302">32</span></span> |
| <span data-ttu-id="937fc-6303">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6303">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6305">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6305">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6306">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6306">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6307">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6307">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6308">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6308">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6309">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6309">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6311">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6311">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6313">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6313">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6315">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6315">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6317">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6317">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-6318">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6318">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-6319">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6319">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6320">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6320">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6321">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6321">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-6322">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6322">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6323">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6323">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6325">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6325">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-6326">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6326">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6327">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6327">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6328">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6328">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6329">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6329">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6330">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6330">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6331">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6331">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6332">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6332">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-6333">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6333">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-6334">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6334">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6335">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6335">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6336">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6336">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6337">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6337">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6338">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6338">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6339">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6339">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6340">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6340">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6341">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6341">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6343">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6343">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6344">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6344">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6345">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6345">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-6346">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6346">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-6347">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6347">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-6348">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6348">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6349">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6349">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6351">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6351">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6352">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6352">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-6353">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6353">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-6354">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6354">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6356">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6356">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6357">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6357">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="937fc-6359">DXGI_FORMAT_B8G8R8X8_UNORM<sup>(</sup> 88)</span><span class="sxs-lookup"><span data-stu-id="937fc-6359">DXGI_FORMAT_B8G8R8X8_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="937fc-6360">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6360">Target</span></span> | <span data-ttu-id="937fc-6361">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6361">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6362">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6362">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6363">32</span><span class="sxs-lookup"><span data-stu-id="937fc-6363">32</span></span> |
| <span data-ttu-id="937fc-6364">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6364">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6366">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6366">Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6368">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6368">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6370">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6370">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6371">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6371">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6372">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6372">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6374">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6374">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6376">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6376">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6378">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6378">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6380">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6380">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6382">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6382">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6384">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6384">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6385">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6385">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6386">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6386">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6388">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6388">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6389">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6389">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6391">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6391">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6393">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6393">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6395">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6395">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6397">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6398">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6399">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6400">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6401">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6401">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-6402">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-6403">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6404">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6405">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6406">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6407">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6408">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6408">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6409">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6409">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6410">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6410">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6412">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6412">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6414">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6414">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6416">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6416">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6418">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6418">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6420">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6420">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6422">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6422">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6423">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6423">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6425">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6425">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6426">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6426">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6428">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6428">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6430">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6430">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6432">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6432">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6433">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6433">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="937fc-6435">DXGI_FORMAT_B8G8R8X8_UNORM_SRGB<sup>(</sup> 93)</span><span class="sxs-lookup"><span data-stu-id="937fc-6435">DXGI_FORMAT_B8G8R8X8_UNORM_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="937fc-6436">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6436">Target</span></span> | <span data-ttu-id="937fc-6437">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6437">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6438">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6438">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6439">32</span><span class="sxs-lookup"><span data-stu-id="937fc-6439">32</span></span> |
| <span data-ttu-id="937fc-6440">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6440">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6442">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6442">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6443">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6443">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6444">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6444">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6445">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6445">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6446">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6446">Texture1D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6448">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6450">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6450">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6452">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6452">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6454">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6454">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6456">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6456">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6458">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6458">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6459">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6459">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6460">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6460">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6462">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6462">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6463">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6463">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6465">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6465">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6467">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6467">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6469">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6469">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6471">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6471">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6472">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6472">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6473">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6473">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6474">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6474">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6475">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6475">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-6476">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6476">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-6477">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6477">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6478">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6478">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6479">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6479">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6480">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6480">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6481">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6481">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6482">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6482">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6483">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6483">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6484">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6484">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6486">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6486">4x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6488">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6488">8x Multisample RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6490">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6490">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6492">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6492">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6494">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6494">Multisample Load</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6496">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6496">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6497">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6497">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6499">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6499">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6500">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6500">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-6501">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6501">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-6502">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6502">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6504">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6504">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6505">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6505">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a><span data-ttu-id="937fc-6507">DXGI_FORMAT_BC6H_TYPELESS<sup>PCC</sup> (94)</span><span class="sxs-lookup"><span data-stu-id="937fc-6507">DXGI_FORMAT_BC6H_TYPELESS<sup>PCC</sup> (94)</span></span>
| <span data-ttu-id="937fc-6508">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6508">Target</span></span> | <span data-ttu-id="937fc-6509">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6509">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6510">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6510">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6511">128</span><span class="sxs-lookup"><span data-stu-id="937fc-6511">128</span></span> |
| <span data-ttu-id="937fc-6512">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6512">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6514">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6514">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6515">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6515">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6516">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6516">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6517">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6517">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6518">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6518">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-6519">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6519">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6521">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6521">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6523">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6523">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6525">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6525">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-6526">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6526">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-6527">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6527">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6528">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6528">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6529">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6529">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-6530">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6530">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6531">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6531">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6533">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6533">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-6534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6534">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6535">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6535">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6536">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6536">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6537">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6537">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6538">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6538">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6539">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6539">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6540">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6540">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-6541">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6541">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-6542">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6542">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6543">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6543">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6544">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6544">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6545">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6545">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6546">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6546">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6547">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6547">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6548">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6548">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6549">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6549">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6551">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6551">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6552">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6552">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6553">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6553">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-6554">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6554">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-6555">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6555">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-6556">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6556">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6557">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6557">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6559">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6559">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6560">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6560">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-6561">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6561">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-6562">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6562">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-6563">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6563">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6564">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6564">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a><span data-ttu-id="937fc-6566">DXGI_FORMAT_BC6H_UF16 <sup>FCC</sup> (95)</span><span class="sxs-lookup"><span data-stu-id="937fc-6566">DXGI_FORMAT_BC6H_UF16 <sup>FCC</sup> (95)</span></span>
| <span data-ttu-id="937fc-6567">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6567">Target</span></span> | <span data-ttu-id="937fc-6568">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6568">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6569">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6569">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6570">128</span><span class="sxs-lookup"><span data-stu-id="937fc-6570">128</span></span> |
| <span data-ttu-id="937fc-6571">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6571">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6573">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6573">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6574">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6574">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6575">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6575">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6576">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6576">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6577">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6577">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-6578">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6578">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6580">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6580">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6582">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6582">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6584">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6584">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6586">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6586">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6588">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6588">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6589">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6589">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6590">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6590">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6592">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6592">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6593">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6593">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6595">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6595">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-6596">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6596">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6597">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6597">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6598">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6598">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6599">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6599">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6600">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6600">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6601">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6601">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6602">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6602">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-6603">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6603">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-6604">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6604">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6605">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6605">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6606">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6606">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6607">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6607">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6608">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6608">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6609">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6609">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6610">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6610">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6611">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6611">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6613">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6613">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6614">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6614">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6615">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6615">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-6616">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6616">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-6617">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6617">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-6618">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6618">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6619">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6619">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6621">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6621">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6622">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6622">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-6623">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6623">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-6624">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6624">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-6625">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6625">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6626">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6626">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a><span data-ttu-id="937fc-6628">DXGI_FORMAT_BC6H_SF16 <sup>FCC</sup> (96)</span><span class="sxs-lookup"><span data-stu-id="937fc-6628">DXGI_FORMAT_BC6H_SF16 <sup>FCC</sup> (96)</span></span>
| <span data-ttu-id="937fc-6629">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6629">Target</span></span> | <span data-ttu-id="937fc-6630">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6630">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6631">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6631">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6632">128</span><span class="sxs-lookup"><span data-stu-id="937fc-6632">128</span></span> |
| <span data-ttu-id="937fc-6633">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6633">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6635">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6635">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6636">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6636">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6637">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6637">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6638">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6638">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6639">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6639">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-6640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6640">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6642">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6644">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6644">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6646">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6646">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6648">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6648">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6650">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6650">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6651">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6651">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6652">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6652">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6654">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6654">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6655">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6655">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6657">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6657">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-6658">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6658">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6659">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6659">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6660">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6660">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6661">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6661">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6662">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6662">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6663">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6663">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6664">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6664">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-6665">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6665">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-6666">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6666">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6667">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6667">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6668">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6668">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6669">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6669">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6670">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6670">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6671">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6671">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6672">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6672">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6673">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6673">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6675">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6675">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6676">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6676">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6677">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6677">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-6678">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6678">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-6679">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6679">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-6680">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6680">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6681">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6681">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6683">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6683">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6684">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6684">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-6685">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6685">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-6686">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6686">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-6687">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6687">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6688">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6688">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a><span data-ttu-id="937fc-6690">DXGI_FORMAT_BC7_TYPELESS<sup>PCC</sup> (97)</span><span class="sxs-lookup"><span data-stu-id="937fc-6690">DXGI_FORMAT_BC7_TYPELESS<sup>PCC</sup> (97)</span></span>
| <span data-ttu-id="937fc-6691">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6691">Target</span></span> | <span data-ttu-id="937fc-6692">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6692">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6693">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6693">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6694">128</span><span class="sxs-lookup"><span data-stu-id="937fc-6694">128</span></span> |
| <span data-ttu-id="937fc-6695">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6695">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6697">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6697">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6698">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6698">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6699">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6699">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6700">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6700">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6701">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6701">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-6702">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6702">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6704">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6704">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6706">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6706">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6708">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6708">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-6709">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6709">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-6710">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6710">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6711">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6711">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6712">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6712">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-6713">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6713">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6714">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6714">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6716">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6716">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-6717">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6717">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6718">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6719">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6720">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6721">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6722">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6723">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6723">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-6724">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-6725">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6726">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6727">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6728">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6729">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6730">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6730">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6731">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6731">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6732">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6732">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6734">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6734">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6735">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6735">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6736">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6736">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-6737">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6737">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-6738">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6738">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-6739">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6739">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6740">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6740">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6742">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6742">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6743">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6743">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-6744">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6744">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-6745">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6745">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-6746">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6746">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6747">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6747">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a><span data-ttu-id="937fc-6749">DXGI_FORMAT_BC7_UNORM <sup>FCC</sup> (98)</span><span class="sxs-lookup"><span data-stu-id="937fc-6749">DXGI_FORMAT_BC7_UNORM <sup>FCC</sup> (98)</span></span>
| <span data-ttu-id="937fc-6750">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6750">Target</span></span> | <span data-ttu-id="937fc-6751">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6751">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6752">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6752">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6753">128</span><span class="sxs-lookup"><span data-stu-id="937fc-6753">128</span></span> |
| <span data-ttu-id="937fc-6754">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6754">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6756">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6756">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6757">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6757">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6758">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6758">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6759">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6759">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6760">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6760">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-6761">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6761">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6763">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6763">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6765">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6765">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6767">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6767">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6769">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6769">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6771">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6771">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6772">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6772">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6773">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6773">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6775">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6775">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6776">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6776">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6778">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6778">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-6779">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6779">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6780">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6780">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6781">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6781">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6782">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6782">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6783">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6783">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6784">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6784">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6785">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6785">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-6786">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6786">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-6787">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6787">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6788">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6788">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6789">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6789">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6790">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6790">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6791">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6791">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6792">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6792">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6793">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6793">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6794">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6794">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6796">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6796">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6797">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6797">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6798">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6798">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-6799">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6799">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-6800">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6800">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-6801">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6801">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6802">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6802">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6804">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6804">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6805">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6805">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-6806">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6806">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-6807">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6807">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-6808">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6808">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6809">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6809">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a><span data-ttu-id="937fc-6811">DXGI_FORMAT_BC7_UNORM_SRGB <sup>FCC</sup> (99)</span><span class="sxs-lookup"><span data-stu-id="937fc-6811">DXGI_FORMAT_BC7_UNORM_SRGB <sup>FCC</sup> (99)</span></span>
| <span data-ttu-id="937fc-6812">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6812">Target</span></span> | <span data-ttu-id="937fc-6813">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6813">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6814">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6814">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6815">128</span><span class="sxs-lookup"><span data-stu-id="937fc-6815">128</span></span> |
| <span data-ttu-id="937fc-6816">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6816">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6818">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6818">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6819">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6819">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6820">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6820">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6821">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6821">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6822">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6822">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-6823">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6823">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6825">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6825">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6827">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6829">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6829">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6831">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6831">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6833">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6833">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6834">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6834">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6835">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6835">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6837">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6837">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6838">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6838">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6840">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6840">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-6841">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6841">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6842">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6842">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6843">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6843">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6844">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6844">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6845">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6845">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6846">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6846">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6847">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6847">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-6848">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6848">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-6849">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6849">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6850">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6850">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6851">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6851">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6852">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6852">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6853">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6853">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6854">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6854">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6855">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6855">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6856">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6856">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6858">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6858">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6859">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6859">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6860">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6860">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-6861">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6861">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-6862">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6862">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-6863">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6863">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6864">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6864">Cast Within Bit Layout</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6866">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6866">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-6867">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6867">Video Processor Input</span></span> | \- |
| <span data-ttu-id="937fc-6868">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6868">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-6869">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6869">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-6870">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6870">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6871">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6871">Tiled Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="937fc-6873">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="937fc-6873">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="937fc-6874">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6874">Target</span></span> | <span data-ttu-id="937fc-6875">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6875">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6876">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6876">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6877">32</span><span class="sxs-lookup"><span data-stu-id="937fc-6877">32</span></span> |
| <span data-ttu-id="937fc-6878">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6878">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6880">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6880">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6881">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6881">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6882">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6882">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6883">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6883">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6884">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6884">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-6885">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6885">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6887">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6887">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-6888">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6888">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-6889">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6889">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6891">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6891">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6893">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6893">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6894">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6894">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6895">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6895">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6897">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6897">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6898">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6898">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6900">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6900">Mipmap Auto- Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6902">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6902">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6904">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6904">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6906">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6906">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6907">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6907">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6908">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6908">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6909">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6909">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6910">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6910">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6912">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6912">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6914">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6914">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6915">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6915">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6916">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6916">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6917">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6917">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6918">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6918">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6919">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6919">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6920">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6920">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6921">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6921">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6923">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6923">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6924">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6924">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6925">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6925">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-6926">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6926">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-6927">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6927">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-6928">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6928">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6929">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6929">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-6930">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6930">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6932">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6932">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6934">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6934">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6936">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6936">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6938">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-6938">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-6939">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6939">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="937fc-6940">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="937fc-6940">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="937fc-6941">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6941">Target</span></span> | <span data-ttu-id="937fc-6942">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-6942">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-6943">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-6943">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-6944">32</span><span class="sxs-lookup"><span data-stu-id="937fc-6944">32</span></span> |
| <span data-ttu-id="937fc-6945">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-6945">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6947">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6947">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6948">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-6948">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6949">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-6949">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6950">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-6950">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-6951">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-6951">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-6952">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-6952">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6954">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-6954">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-6955">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-6955">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-6956">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-6956">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6958">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6958">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6960">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6960">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-6961">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-6961">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-6962">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-6962">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6964">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-6964">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-6965">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6965">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-6966">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-6966">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-6967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6967">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6968">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6968">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6969">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-6969">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-6970">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-6970">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-6971">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6971">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6972">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-6972">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-6973">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-6973">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6975">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-6975">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6977">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6977">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-6978">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-6978">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-6979">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-6979">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-6980">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-6980">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-6981">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-6981">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-6982">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-6982">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6983">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-6983">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-6984">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-6984">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-6986">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6986">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6987">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-6987">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-6988">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-6988">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-6989">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-6989">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-6990">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-6990">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-6991">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-6991">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-6992">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-6992">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-6993">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-6993">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6995">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6995">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6997">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-6997">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-6999">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-6999">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7001">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7001">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7002">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7002">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="937fc-7003">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="937fc-7003">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="937fc-7004">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7004">Target</span></span> | <span data-ttu-id="937fc-7005">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7005">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7006">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7006">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7007">64</span><span class="sxs-lookup"><span data-stu-id="937fc-7007">64</span></span> |
| <span data-ttu-id="937fc-7008">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7008">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7010">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7010">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7011">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7011">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7012">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7012">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7013">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7013">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7014">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7014">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7015">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7015">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7017">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7017">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7018">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7018">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7019">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7019">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7021">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7021">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7023">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7023">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7024">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7024">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7025">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7025">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7027">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7027">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7028">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7028">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7030">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7030">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7031">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7031">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7032">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7032">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7033">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7033">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7034">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7034">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7035">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7035">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7036">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7036">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7037">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7037">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7039">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7039">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7041">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7041">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7042">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7042">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7043">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7043">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7044">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7044">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7045">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7045">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7046">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7046">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7047">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7047">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7048">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7048">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7050">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7050">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7051">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7051">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7052">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7052">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7053">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7053">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7054">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7054">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7055">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7055">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7056">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7056">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7057">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7057">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7059">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7059">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7061">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7061">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7063">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7063">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7065">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7065">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7066">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7066">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="937fc-7067">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="937fc-7067">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="937fc-7068">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7068">Target</span></span> | <span data-ttu-id="937fc-7069">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7069">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7070">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7070">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7071">8</span><span class="sxs-lookup"><span data-stu-id="937fc-7071">8</span></span> |
| <span data-ttu-id="937fc-7072">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7072">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7074">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7074">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7075">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7075">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7076">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7076">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7077">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7077">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7078">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7078">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7079">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7079">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7081">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7081">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7082">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7082">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7083">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7083">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7085">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7085">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7087">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7087">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7088">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7088">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7089">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7089">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7091">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7091">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7092">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7092">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-7093">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7093">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7094">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7094">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7096">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7096">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7098">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7099">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7100">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7101">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7102">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7102">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7104">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7104">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7106">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7106">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7107">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7107">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7108">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7108">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7109">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7109">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7110">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7110">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7111">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7111">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7112">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7112">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7113">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7113">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7115">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7116">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7117">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7118">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7119">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7119">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7120">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7121">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7122">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7122">Video Decoder Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7124">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7124">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7126">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7126">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7128">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7128">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7130">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7130">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7131">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7131">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="937fc-7132">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="937fc-7132">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="937fc-7133">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7133">Target</span></span> | <span data-ttu-id="937fc-7134">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7134">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7135">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7135">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7136">16</span><span class="sxs-lookup"><span data-stu-id="937fc-7136">16</span></span> |
| <span data-ttu-id="937fc-7137">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7137">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7139">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7139">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7140">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7140">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7141">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7141">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7142">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7142">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7143">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7143">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7144">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7146">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7147">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7147">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7148">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7148">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7150">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7150">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7152">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7152">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7153">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7153">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7154">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7154">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7156">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7156">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7157">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7157">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-7158">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7158">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7159">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7159">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7161">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7161">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7163">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7164">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7165">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7166">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7167">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7167">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7169">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7169">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7171">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7172">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7173">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7174">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7175">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7176">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7176">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7177">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7177">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7178">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7178">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7180">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7180">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7181">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7181">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7182">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7182">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7183">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7183">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7184">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7184">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7185">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7185">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7186">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7186">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7187">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7187">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7189">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7189">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7191">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7191">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7193">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7193">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7195">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7195">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7196">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7196">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="937fc-7197">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="937fc-7197">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="937fc-7198">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7198">Target</span></span> | <span data-ttu-id="937fc-7199">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7199">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7200">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7200">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7201">16</span><span class="sxs-lookup"><span data-stu-id="937fc-7201">16</span></span> |
| <span data-ttu-id="937fc-7202">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7202">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7204">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7204">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7205">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7205">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7206">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7206">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7207">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7207">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7208">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7208">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7209">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7209">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7211">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7211">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7212">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7212">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7213">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7213">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7215">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7215">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7217">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7217">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7218">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7218">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7219">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7219">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7221">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7221">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7222">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7222">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-7223">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7223">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7224">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7224">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7226">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7226">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7228">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7228">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7229">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7229">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7230">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7230">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7231">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7231">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7232">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7232">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7234">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7234">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7236">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7237">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7238">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7239">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7240">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7241">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7241">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7242">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7242">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7243">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7243">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7245">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7246">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7247">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7248">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7249">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7249">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7250">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7251">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7252">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7252">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7254">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7254">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7256">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7256">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7258">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7258">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7260">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7260">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7261">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7261">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="937fc-7262">DXGI_FORMAT_420_OPAQUE<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="937fc-7262">DXGI_FORMAT_420_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="937fc-7263">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7263">Target</span></span> | <span data-ttu-id="937fc-7264">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7264">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7265">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7265">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7266">8</span><span class="sxs-lookup"><span data-stu-id="937fc-7266">8</span></span> |
| <span data-ttu-id="937fc-7267">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7267">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7269">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7269">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7270">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7270">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7271">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7271">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7272">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7272">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7273">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7273">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7274">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7274">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7276">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7276">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7277">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7277">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7278">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7278">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-7279">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7279">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-7280">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7280">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7281">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7281">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7282">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7282">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-7283">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7283">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7284">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7284">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-7285">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7285">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7286">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7286">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7287">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7287">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7288">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7288">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7289">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7289">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7290">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7290">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7291">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7291">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7292">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7292">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-7293">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7293">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-7294">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7294">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7295">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7295">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7296">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7296">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7297">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7297">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7298">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7298">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7299">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7299">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7300">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7300">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7301">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7301">CPU Lockable</span></span> | \- |
| <span data-ttu-id="937fc-7302">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7302">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7303">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7303">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7304">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7304">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7305">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7305">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7306">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7306">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7307">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7307">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7308">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7308">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7309">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7309">Video Decoder Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7311">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7311">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7313">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7313">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7315">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7315">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7317">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7317">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7318">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7318">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="937fc-7319">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="937fc-7319">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="937fc-7320">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7320">Target</span></span> | <span data-ttu-id="937fc-7321">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7321">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7322">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7322">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7323">16</span><span class="sxs-lookup"><span data-stu-id="937fc-7323">16</span></span> |
| <span data-ttu-id="937fc-7324">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7324">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7326">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7326">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7327">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7327">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7328">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7328">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7329">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7329">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7330">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7330">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7331">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7331">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7333">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7333">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7334">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7334">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7335">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7335">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7337">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7337">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7339">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7339">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7340">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7340">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7341">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7341">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7343">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7343">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7344">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7344">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-7345">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7345">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7346">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7346">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7347">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7347">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7348">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7348">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7349">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7349">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7350">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7350">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7351">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7351">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7352">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7352">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7354">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7354">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7356">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7356">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7357">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7357">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7358">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7358">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7359">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7359">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7360">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7360">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7361">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7361">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7362">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7362">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7363">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7363">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7365">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7365">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7366">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7366">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7367">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7367">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7368">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7369">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7369">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7370">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7370">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7371">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7371">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7372">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7372">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7374">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7374">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7376">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7376">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7378">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7378">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7380">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7380">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7381">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7381">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="937fc-7382">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="937fc-7382">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="937fc-7383">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7383">Target</span></span> | <span data-ttu-id="937fc-7384">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7384">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7385">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7385">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7386">32</span><span class="sxs-lookup"><span data-stu-id="937fc-7386">32</span></span> |
| <span data-ttu-id="937fc-7387">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7387">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7389">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7389">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7390">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7390">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7391">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7391">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7392">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7392">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7393">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7393">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7394">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7394">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7396">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7396">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7397">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7397">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7398">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7398">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7400">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7400">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7402">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7402">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7403">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7403">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7404">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7404">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7406">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7406">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7407">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7407">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-7408">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7408">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7409">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7410">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7411">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7412">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7413">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7414">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7415">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7415">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7417">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7417">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7419">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7419">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7420">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7420">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7421">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7421">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7422">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7422">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7423">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7423">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7424">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7424">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7425">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7425">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7426">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7426">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7428">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7429">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7430">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7431">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7432">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7432">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7433">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7434">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7435">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7435">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7437">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7437">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7439">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7439">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7441">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7441">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7443">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7443">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7444">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7444">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="937fc-7445">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="937fc-7445">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="937fc-7446">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7446">Target</span></span> | <span data-ttu-id="937fc-7447">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7447">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7448">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7448">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7449">32</span><span class="sxs-lookup"><span data-stu-id="937fc-7449">32</span></span> |
| <span data-ttu-id="937fc-7450">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7450">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7452">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7452">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7453">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7453">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7454">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7454">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7455">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7455">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7456">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7456">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7457">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7457">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7459">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7459">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7460">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7460">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7461">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7461">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7463">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7463">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7465">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7465">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7466">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7466">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7467">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7467">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7469">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7469">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7470">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7470">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-7471">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7471">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7472">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7472">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7473">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7473">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7474">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7474">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7475">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7475">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7476">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7476">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7477">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7477">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7478">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7478">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7480">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7480">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7482">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7482">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7483">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7483">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7484">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7484">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7485">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7485">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7486">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7486">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7487">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7487">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7488">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7488">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7489">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7489">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7491">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7491">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7492">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7492">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7493">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7493">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7494">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7494">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7495">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7495">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7496">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7496">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7497">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7497">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7498">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7498">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7500">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7500">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7502">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7502">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7504">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7504">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7506">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7506">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7507">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7507">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="937fc-7508">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="937fc-7508">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="937fc-7509">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7509">Target</span></span> | <span data-ttu-id="937fc-7510">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7510">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7511">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7511">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7512">8</span><span class="sxs-lookup"><span data-stu-id="937fc-7512">8</span></span> |
| <span data-ttu-id="937fc-7513">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7513">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7515">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7515">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7516">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7516">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7517">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7517">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7518">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7518">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7519">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7519">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7520">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7520">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7522">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7522">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7523">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7523">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7524">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7524">Shader ld</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7526">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7526">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7528">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7528">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7529">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7529">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7530">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7530">Shader gather4</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7532">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7532">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7533">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7533">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-7534">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7534">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7535">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7535">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7537">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7537">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7539">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7539">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7540">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7540">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7541">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7541">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7542">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7542">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7543">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7543">Typed UAV</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7545">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7545">UAV Typed Store</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7547">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7547">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7548">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7548">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7549">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7549">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7550">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7550">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7551">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7551">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7552">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7552">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7553">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7553">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7554">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7554">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7556">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7556">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7557">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7557">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7558">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7558">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7559">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7559">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7560">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7560">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7561">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7561">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7562">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7562">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7563">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7563">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7565">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7565">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7567">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7567">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7569">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7569">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7571">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7571">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7572">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7572">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="937fc-7573">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="937fc-7573">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="937fc-7574">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7574">Target</span></span> | <span data-ttu-id="937fc-7575">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7575">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7576">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7576">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7577">8</span><span class="sxs-lookup"><span data-stu-id="937fc-7577">8</span></span> |
| <span data-ttu-id="937fc-7578">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7578">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7580">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7580">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7581">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7581">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7582">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7583">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7583">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7584">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7584">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7585">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7585">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7587">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7587">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7588">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7588">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7589">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7589">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-7590">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7590">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-7591">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7591">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7592">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7592">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7593">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7593">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-7594">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7594">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7595">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7595">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-7596">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7596">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7597">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7597">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7598">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7598">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7599">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7599">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7600">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7600">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7601">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7601">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7602">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7602">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7603">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7603">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-7604">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7604">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-7605">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7605">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7606">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7606">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7607">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7607">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7608">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7608">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7609">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7609">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7610">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7610">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7611">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7611">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7612">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7612">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7614">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7614">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7615">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7615">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7616">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7616">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7617">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7617">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7618">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7618">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7619">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7619">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7620">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7620">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7621">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7621">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-7622">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7622">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7624">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7624">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-7625">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7625">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-7626">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7626">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7627">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7627">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="937fc-7628">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="937fc-7628">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="937fc-7629">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7629">Target</span></span> | <span data-ttu-id="937fc-7630">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7630">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7631">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7631">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7632">8</span><span class="sxs-lookup"><span data-stu-id="937fc-7632">8</span></span> |
| <span data-ttu-id="937fc-7633">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7633">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7635">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7635">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7636">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7636">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7637">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7637">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7638">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7638">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7639">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7639">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7640">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7642">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7643">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7643">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7644">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7644">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-7645">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7645">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-7646">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7646">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7647">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7647">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7648">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7648">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-7649">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7649">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7650">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7650">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-7651">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7651">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7652">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7652">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7653">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7653">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7654">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7654">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7655">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7655">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7656">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7656">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7657">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7657">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7658">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7658">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-7659">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7659">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-7660">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7660">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7661">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7661">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7662">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7662">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7663">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7663">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7664">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7664">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7665">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7665">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7666">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7666">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7667">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7667">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7669">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7669">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7670">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7670">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7671">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7671">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7672">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7672">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7673">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7673">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7674">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7674">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7675">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7675">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7676">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7676">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-7677">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7677">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7679">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-7680">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7680">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-7681">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7681">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7682">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="937fc-7683">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="937fc-7683">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="937fc-7684">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7684">Target</span></span> | <span data-ttu-id="937fc-7685">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7685">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7686">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7687">8</span><span class="sxs-lookup"><span data-stu-id="937fc-7687">8</span></span> |
| <span data-ttu-id="937fc-7688">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7688">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7690">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7690">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7691">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7691">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7692">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7692">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7693">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7693">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7694">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7694">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7695">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7695">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7697">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7697">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7698">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7698">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7699">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7699">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-7700">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7700">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-7701">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7701">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7702">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7702">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7703">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7703">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-7704">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7704">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7705">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7705">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-7706">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7706">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7707">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7707">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7708">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7708">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7709">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7709">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7710">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7710">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7711">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7711">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7712">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7712">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7713">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7713">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-7714">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7714">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-7715">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7715">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7716">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7716">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7717">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7717">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7718">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7718">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7719">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7719">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7720">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7720">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7721">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7721">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7722">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7722">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7724">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7724">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7725">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7725">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7726">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7726">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7727">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7727">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7728">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7728">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7729">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7729">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7730">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7730">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7731">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7731">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-7732">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7732">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7734">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7734">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-7735">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7735">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-7736">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7736">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7737">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7737">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="937fc-7738">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="937fc-7738">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="937fc-7739">Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7739">Target</span></span> | <span data-ttu-id="937fc-7740">Support</span><span class="sxs-lookup"><span data-stu-id="937fc-7740">Support</span></span> |
| - | - |
| <span data-ttu-id="937fc-7741">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="937fc-7741">Bits Per Element (BPE)</span></span> | <span data-ttu-id="937fc-7742">16</span><span class="sxs-lookup"><span data-stu-id="937fc-7742">16</span></span> |
| <span data-ttu-id="937fc-7743">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="937fc-7743">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="937fc-7745">Buffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7745">Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7746">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="937fc-7746">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7747">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="937fc-7747">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7748">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="937fc-7748">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="937fc-7749">Texture1D</span><span class="sxs-lookup"><span data-stu-id="937fc-7749">Texture1D</span></span> | \- |
| <span data-ttu-id="937fc-7750">Texture2D</span><span class="sxs-lookup"><span data-stu-id="937fc-7750">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7752">Texture3D</span><span class="sxs-lookup"><span data-stu-id="937fc-7752">Texture3D</span></span> | \- |
| <span data-ttu-id="937fc-7753">TextureCube</span><span class="sxs-lookup"><span data-stu-id="937fc-7753">TextureCube</span></span> | \- |
| <span data-ttu-id="937fc-7754">Shader LD</span><span class="sxs-lookup"><span data-stu-id="937fc-7754">Shader ld</span></span> | \- |
| <span data-ttu-id="937fc-7755">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7755">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="937fc-7756">Shader-sample_c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7756">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="937fc-7757">Shader-Beispiel (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="937fc-7757">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="937fc-7758">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="937fc-7758">Shader gather4</span></span> | \- |
| <span data-ttu-id="937fc-7759">Shader-gather4_c</span><span class="sxs-lookup"><span data-stu-id="937fc-7759">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="937fc-7760">MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7760">Mipmap</span></span> | \- |
| <span data-ttu-id="937fc-7761">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="937fc-7761">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="937fc-7762">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7762">RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7763">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7763">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7764">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="937fc-7764">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="937fc-7765">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="937fc-7765">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="937fc-7766">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7766">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7767">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="937fc-7767">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="937fc-7768">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="937fc-7768">Typed UAV</span></span> | \- |
| <span data-ttu-id="937fc-7769">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="937fc-7769">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="937fc-7770">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7770">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="937fc-7771">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="937fc-7771">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="937fc-7772">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="937fc-7772">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="937fc-7773">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="937fc-7773">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="937fc-7774">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="937fc-7774">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="937fc-7775">UAV-atomarischer Mindestwert/max.</span><span class="sxs-lookup"><span data-stu-id="937fc-7775">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7776">UAV-atomarische unsignierte Min/Max</span><span class="sxs-lookup"><span data-stu-id="937fc-7776">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="937fc-7777">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="937fc-7777">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7779">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7779">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7780">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="937fc-7780">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="937fc-7781">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="937fc-7781">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="937fc-7782">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="937fc-7782">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="937fc-7783">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="937fc-7783">Multisample Load</span></span> | \- |
| <span data-ttu-id="937fc-7784">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="937fc-7784">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="937fc-7785">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="937fc-7785">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="937fc-7786">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="937fc-7786">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="937fc-7787">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7787">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="937fc-7789">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="937fc-7789">Video Processor Output</span></span> | \- |
| <span data-ttu-id="937fc-7790">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7790">Shared Resource</span></span> | \- |
| <span data-ttu-id="937fc-7791">BackBuffer-castfähig, auch vollständig typisiert</span><span class="sxs-lookup"><span data-stu-id="937fc-7791">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="937fc-7792">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="937fc-7792">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="937fc-7793">Notizen formatieren</span><span class="sxs-lookup"><span data-stu-id="937fc-7793">Format notes</span></span>

<span data-ttu-id="937fc-7794">Der Zweck des-Formats kann sich von einer Hardware Funktionsebene zur nächsten ändern.</span><span class="sxs-lookup"><span data-stu-id="937fc-7794">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="937fc-7795"><sup>L</sup> : typloses Format</span><span class="sxs-lookup"><span data-stu-id="937fc-7795"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="937fc-7796"><sup>PCs</sup> : teilweise typisiertes, castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="937fc-7796"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="937fc-7797"><sup>FCS</sup> : vollständig typisiertes, castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="937fc-7797"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="937fc-7798"><sup>FNS</sup> : vollständig typisiertes, nicht-castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="937fc-7798"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="937fc-7799"><sup>PCC</sup> : teilweise typisiertes, castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="937fc-7799"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="937fc-7800"><sup>FCC</sup> : vollständig typisiertes, castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="937fc-7800"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="937fc-7801"><sup>FNC</sup> : vollständig typisiertes, nicht-castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="937fc-7801"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="937fc-7802"><sup>V</sup> : Videoformat</span><span class="sxs-lookup"><span data-stu-id="937fc-7802"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="dxgi_format_related-topics"></a><span data-ttu-id="937fc-7803">Themen zu DXGI_FORMAT_Related</span><span class="sxs-lookup"><span data-stu-id="937fc-7803">DXGI_FORMAT_Related topics</span></span>

[<span data-ttu-id="937fc-7804">D3D12-Hardware Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="937fc-7804">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="937fc-7805">Programmier Handbuch für DXGI</span><span class="sxs-lookup"><span data-stu-id="937fc-7805">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
