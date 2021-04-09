---
description: In diesem Abschnitt werden die Formate ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die in der Direct3D-Funktion 10level9 9,1-Hardware unterstützt werden.
ms.assetid: 770A5396-C5D9-442B-99FE-3D220C54E8EB
title: Formatunterstützung für Direct3D 9 9.1-Hardware auf Featureebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56653fd2fb504e3f23cfac13b432530ebaa7219b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860129"
---
# <a name="format-support-for-direct3d-feature-10level9-91-hardware"></a><span data-ttu-id="13900-103">Formatunterstützung für Direct3D 9 9.1-Hardware auf Featureebene</span><span class="sxs-lookup"><span data-stu-id="13900-103">Format support for Direct3D Feature 10Level9 9.1 hardware</span></span>

<span data-ttu-id="13900-104">In diesem Abschnitt werden die Formate ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die in der Direct3D-Funktion 10level9 9,1-Hardware unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="13900-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.1 hardware.</span></span>

<span data-ttu-id="13900-105">Die Tabelle enthält eine Zusammenfassung der Featureunterstützung, die den folgenden Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="13900-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="13900-106">Symbol</span><span class="sxs-lookup"><span data-stu-id="13900-106">Symbol</span></span>                            | <span data-ttu-id="13900-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13900-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="13900-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="13900-108">_ *-*\*</span></span>                             | <span data-ttu-id="13900-109">Nicht zulässig oder nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="13900-109">Disallowed or not available.</span></span>                                                  |
| ![Erforderlich](images/letter-r.jpg)  | <span data-ttu-id="13900-111">Hardware Unterstützung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="13900-111">Hardware support is required.</span></span>                                                 |
| ![Optional](images/letter-o.jpg)  | <span data-ttu-id="13900-113">Hardwareunterstützung optional, das Format ist möglicherweise Hardware beschleunigt.</span><span class="sxs-lookup"><span data-stu-id="13900-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![lässe](images/letter-d.jpg) | <span data-ttu-id="13900-115">Erforderlich, wenn eine zugehörige optionale Funktion unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="13900-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="13900-116">Dieses Thema enthält einen Abschnitt Pro Format.</span><span class="sxs-lookup"><span data-stu-id="13900-116">This topic contains a section per format.</span></span> <span data-ttu-id="13900-117">Ein Format *Ziel* (die Tabellen enthalten eine Zeile pro Ziel) kann ein Ressourcentyp, eine intrinsische HLSL-Funktion oder eine bestimmte Funktionalität sein, die von einem bestimmten Format abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="13900-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="13900-118">Informationen zur programmgesteuerten Überprüfung der Formatunterstützung in D3D11 und D3D12 finden Sie unter über [Prüfen der Unterstützung von Hardwarefunktionen](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="13900-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="13900-119">Die Zahlen der Formate sind größtenteils, aber nicht alle in aufsteigender numerischer Reihenfolge, dass einige nicht in &mdash; numerischer Reihenfolge sind und neben anderen relevanten Formaten aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="13900-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="13900-120">Beachten Sie auch, dass *typlose* in einem Format Namen *teilweise* typisiert und nicht streng typlos sein kann (Weitere Informationen finden Sie im Abschnitt " [Format Notizen](#format-notes) " am Ende des Themas).</span><span class="sxs-lookup"><span data-stu-id="13900-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

// 

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="13900-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="13900-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="13900-122">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-122">Target</span></span> | <span data-ttu-id="13900-123">Support</span><span class="sxs-lookup"><span data-stu-id="13900-123">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-124">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-125">0</span><span class="sxs-lookup"><span data-stu-id="13900-125">0</span></span> |
| <span data-ttu-id="13900-126">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-126">Format Support</span></span> | \- |
| <span data-ttu-id="13900-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-127">Buffer</span></span> | \- |
| <span data-ttu-id="13900-128">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-129">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-130">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-131">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-132">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-133">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-134">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-135">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-136">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-137">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-138">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-139">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-140">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-141">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-141">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-142">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-144">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-145">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-146">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-147">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-148">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-149">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-150">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-151">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-152">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-153">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-155">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-156">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-157">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-158">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-159">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-160">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-161">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-162">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-163">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-164">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-165">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-166">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-167">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-168">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-169">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-170">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="13900-171">DXGI_FORMAT_R32G32B32A32 \_ Typen losen<sup>PCs</sup> (1)</span><span class="sxs-lookup"><span data-stu-id="13900-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="13900-172">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-172">Target</span></span> | <span data-ttu-id="13900-173">Support</span><span class="sxs-lookup"><span data-stu-id="13900-173">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-174">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-175">128</span><span class="sxs-lookup"><span data-stu-id="13900-175">128</span></span> |
| <span data-ttu-id="13900-176">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-176">Format Support</span></span> | \- |
| <span data-ttu-id="13900-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-177">Buffer</span></span> | \- |
| <span data-ttu-id="13900-178">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-179">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-180">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-181">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-182">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-183">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-184">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-185">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-186">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-187">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-188">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-189">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-190">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-191">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-191">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-192">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-194">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-195">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-196">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-197">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-198">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-199">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-200">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-201">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-202">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-203">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-204">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-205">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-206">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-207">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-208">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-209">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-210">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-211">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-212">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-213">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-214">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-215">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-216">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-217">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-218">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-219">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-220">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="13900-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup></sup> -Datentyp (2)</span><span class="sxs-lookup"><span data-stu-id="13900-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="13900-222">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-222">Target</span></span> | <span data-ttu-id="13900-223">Support</span><span class="sxs-lookup"><span data-stu-id="13900-223">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-224">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-225">128</span><span class="sxs-lookup"><span data-stu-id="13900-225">128</span></span> |
| <span data-ttu-id="13900-226">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-226">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-228">Buffer</span></span> | \- |
| <span data-ttu-id="13900-229">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-229">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-231">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-232">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-233">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-234">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-235">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-235">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-236">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-236">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-237">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-237">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-238">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-238">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-239">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-239">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-240">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-240">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-241">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-241">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-242">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-242">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-243">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-243">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-244">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-244">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-245">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-245">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-246">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-246">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-247">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-247">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-248">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-248">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-249">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-249">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-250">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-250">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-251">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-251">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-252">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-252">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-253">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-253">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-254">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-254">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-255">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-255">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-256">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-256">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-257">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-257">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-258">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-258">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-259">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-259">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-260">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-260">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-261">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-261">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-262">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-262">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-263">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-263">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-264">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-264">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-265">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-265">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-266">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-266">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-267">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-267">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-268">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-268">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-269">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-269">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-270">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-270">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-271">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-271">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-272">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-272">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="13900-273">DXGI_FORMAT_R32G32B32A32 \_ uint<sup></sup> -Benutzerkonten (3)</span><span class="sxs-lookup"><span data-stu-id="13900-273">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="13900-274">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-274">Target</span></span> | <span data-ttu-id="13900-275">Support</span><span class="sxs-lookup"><span data-stu-id="13900-275">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-276">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-276">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-277">128</span><span class="sxs-lookup"><span data-stu-id="13900-277">128</span></span> |
| <span data-ttu-id="13900-278">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-278">Format Support</span></span> | \- |
| <span data-ttu-id="13900-279">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-279">Buffer</span></span> | \- |
| <span data-ttu-id="13900-280">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-281">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-282">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-283">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-284">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-285">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-286">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-287">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-287">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-288">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-288">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-289">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-289">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-290">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-290">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-291">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-291">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-292">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-292">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-293">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-293">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-294">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-294">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-295">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-295">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-296">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-296">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-297">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-297">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-298">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-298">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-299">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-299">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-300">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-300">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-301">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-301">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-302">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-302">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-303">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-303">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-304">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-304">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-305">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-305">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-306">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-306">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-307">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-307">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-308">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-308">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-309">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-309">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-310">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-310">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-311">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-311">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-312">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-312">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-313">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-313">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-314">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-314">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-315">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-315">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-316">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-316">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-317">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-317">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-318">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-318">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-319">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-319">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-320">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-320">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-321">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-321">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-322">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-322">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="13900-323">DXGI_FORMAT_R32G32B32A32 \_ Sint<sup></sup> (4)</span><span class="sxs-lookup"><span data-stu-id="13900-323">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="13900-324">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-324">Target</span></span> | <span data-ttu-id="13900-325">Support</span><span class="sxs-lookup"><span data-stu-id="13900-325">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-326">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-326">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-327">128</span><span class="sxs-lookup"><span data-stu-id="13900-327">128</span></span> |
| <span data-ttu-id="13900-328">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-328">Format Support</span></span> | \- |
| <span data-ttu-id="13900-329">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-329">Buffer</span></span> | \- |
| <span data-ttu-id="13900-330">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-330">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-331">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-332">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-333">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-334">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-335">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-335">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-336">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-337">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-337">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-338">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-338">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-339">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-339">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-340">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-340">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-341">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-341">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-342">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-342">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-343">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-343">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-344">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-345">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-346">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-347">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-348">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-349">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-350">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-351">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-351">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-352">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-353">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-354">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-355">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-356">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-356">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-357">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-358">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-359">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-360">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-360">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-361">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-361">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-362">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-362">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-363">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-363">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-364">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-364">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-365">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-365">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-366">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-366">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-367">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-367">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-368">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-369">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-370">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-371">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-371">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-372">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="13900-373">DXGI_FORMAT_R32G32B32 \_ Typen losen<sup>PCs</sup> (5)</span><span class="sxs-lookup"><span data-stu-id="13900-373">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="13900-374">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-374">Target</span></span> | <span data-ttu-id="13900-375">Support</span><span class="sxs-lookup"><span data-stu-id="13900-375">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-376">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-377">96</span><span class="sxs-lookup"><span data-stu-id="13900-377">96</span></span> |
| <span data-ttu-id="13900-378">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-378">Format Support</span></span> | \- |
| <span data-ttu-id="13900-379">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-379">Buffer</span></span> | \- |
| <span data-ttu-id="13900-380">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-381">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-382">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-383">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-384">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-385">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-385">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-386">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-387">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-387">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-388">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-388">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-389">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-389">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-390">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-390">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-391">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-391">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-392">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-392">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-393">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-393">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-394">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-394">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-395">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-395">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-396">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-396">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-397">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-398">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-399">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-400">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-401">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-401">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-402">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-403">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-404">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-405">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-406">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-407">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-408">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-408">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-409">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-409">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-410">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-410">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-411">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-411">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-412">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-412">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-413">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-413">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-414">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-414">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-415">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-415">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-416">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-416">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-417">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-417">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-418">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-418">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-419">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-419">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-420">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-420">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-421">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-421">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-422">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="13900-423">DXGI_FORMAT_R32G32B32 \_ float<sup></sup> -Datentyp (6)</span><span class="sxs-lookup"><span data-stu-id="13900-423">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="13900-424">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-424">Target</span></span> | <span data-ttu-id="13900-425">Support</span><span class="sxs-lookup"><span data-stu-id="13900-425">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-426">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-427">96</span><span class="sxs-lookup"><span data-stu-id="13900-427">96</span></span> |
| <span data-ttu-id="13900-428">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-428">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-430">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-430">Buffer</span></span> | \- |
| <span data-ttu-id="13900-431">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-431">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-433">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-433">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-434">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-434">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-435">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-435">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-436">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-436">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-437">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-438">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-439">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-440">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-441">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-442">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-443">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-443">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-444">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-445">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-445">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-446">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-447">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-448">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-448">Blendable RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="13900-450">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-450">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-451">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-451">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-452">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-452">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-453">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-453">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-454">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-454">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-455">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-455">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-456">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-456">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-457">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-457">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-458">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-458">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-459">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-459">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-460">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-460">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-461">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-461">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-462">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-462">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-463">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-463">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-464">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-464">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="13900-466">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-466">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="13900-468">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-468">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-469">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-469">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-470">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-470">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-471">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-471">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-472">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-472">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-473">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-473">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-474">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-474">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-475">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-475">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-476">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-476">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-477">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-477">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="13900-478">DXGI_FORMAT_R32G32B32 \_ uint<sup></sup> -(7)</span><span class="sxs-lookup"><span data-stu-id="13900-478">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="13900-479">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-479">Target</span></span> | <span data-ttu-id="13900-480">Support</span><span class="sxs-lookup"><span data-stu-id="13900-480">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-481">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-481">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-482">96</span><span class="sxs-lookup"><span data-stu-id="13900-482">96</span></span> |
| <span data-ttu-id="13900-483">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-483">Format Support</span></span> | \- |
| <span data-ttu-id="13900-484">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-484">Buffer</span></span> | \- |
| <span data-ttu-id="13900-485">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-485">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-486">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-486">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-487">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-487">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-488">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-488">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-489">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-489">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-490">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-491">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-491">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-492">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-492">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-493">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-493">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-494">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-494">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-495">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-495">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-496">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-496">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-497">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-497">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-498">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-498">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-499">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-499">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-500">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-500">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-501">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-501">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-502">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-502">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-503">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-503">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-504">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-504">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-505">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-505">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-506">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-506">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-507">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-507">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-508">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-508">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-509">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-509">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-510">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-510">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-511">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-511">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-512">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-512">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-513">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-513">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-514">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-514">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-515">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-515">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-516">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-516">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="13900-518">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-518">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="13900-520">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-520">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-521">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-521">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-522">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-522">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-523">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-523">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-524">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-524">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-525">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-526">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-527">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-528">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-528">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-529">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-529">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="13900-530">DXGI_FORMAT_R32G32B32 \_ Sint<sup></sup> (8)</span><span class="sxs-lookup"><span data-stu-id="13900-530">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="13900-531">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-531">Target</span></span> | <span data-ttu-id="13900-532">Support</span><span class="sxs-lookup"><span data-stu-id="13900-532">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-533">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-533">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-534">96</span><span class="sxs-lookup"><span data-stu-id="13900-534">96</span></span> |
| <span data-ttu-id="13900-535">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-535">Format Support</span></span> | \- |
| <span data-ttu-id="13900-536">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-536">Buffer</span></span> | \- |
| <span data-ttu-id="13900-537">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-537">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-538">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-539">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-540">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-541">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-541">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-542">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-542">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-543">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-544">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-544">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-545">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-545">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-546">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-546">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-547">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-547">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-548">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-548">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-549">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-549">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-550">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-550">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-551">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-551">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-552">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-552">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-553">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-553">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-554">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-554">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-555">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-555">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-556">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-556">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-557">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-557">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-558">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-558">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-559">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-559">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-560">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-560">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-561">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-561">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-562">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-562">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-563">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-563">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-564">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-564">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-565">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-565">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-566">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-566">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-567">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-567">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-568">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-568">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="13900-570">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-570">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="13900-572">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-572">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-573">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-573">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-574">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-574">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-575">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-575">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-576">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-576">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-577">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-577">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-578">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-578">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-579">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-579">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-580">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-580">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-581">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-581">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="13900-582">DXGI_FORMAT_R16G16B16A16 \_ Typen losen<sup>PCs</sup> (9)</span><span class="sxs-lookup"><span data-stu-id="13900-582">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="13900-583">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-583">Target</span></span> | <span data-ttu-id="13900-584">Support</span><span class="sxs-lookup"><span data-stu-id="13900-584">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-585">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-585">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-586">64</span><span class="sxs-lookup"><span data-stu-id="13900-586">64</span></span> |
| <span data-ttu-id="13900-587">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-587">Format Support</span></span> | \- |
| <span data-ttu-id="13900-588">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-588">Buffer</span></span> | \- |
| <span data-ttu-id="13900-589">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-589">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-590">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-590">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-591">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-591">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-592">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-592">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-593">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-593">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-594">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-594">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-595">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-595">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-596">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-596">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-597">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-597">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-598">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-598">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-599">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-599">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-600">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-600">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-601">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-601">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-602">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-602">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-603">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-603">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-604">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-604">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-605">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-606">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-606">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-607">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-607">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-608">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-608">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-609">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-609">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-610">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-610">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-611">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-611">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-612">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-612">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-613">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-613">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-614">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-614">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-615">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-615">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-616">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-616">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-617">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-617">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-618">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-618">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-619">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-619">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-620">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-620">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-621">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-621">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-622">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-622">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-623">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-623">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-624">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-624">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-625">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-625">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-626">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-626">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-627">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-627">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-628">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-628">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-629">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-629">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-630">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-630">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-631">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-631">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="13900-632">DXGI_FORMAT_R16G16B16A16 float-Dateinamen \_ (10)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="13900-632">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="13900-633">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-633">Target</span></span> | <span data-ttu-id="13900-634">Support</span><span class="sxs-lookup"><span data-stu-id="13900-634">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-635">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-635">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-636">64</span><span class="sxs-lookup"><span data-stu-id="13900-636">64</span></span> |
| <span data-ttu-id="13900-637">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-637">Format Support</span></span> | \- |
| <span data-ttu-id="13900-638">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-638">Buffer</span></span> | \- |
| <span data-ttu-id="13900-639">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-639">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-640">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-640">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-641">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-641">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-642">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-642">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-643">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-643">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-644">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-644">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-645">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-645">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-646">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-646">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-647">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-647">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-648">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-649">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-650">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-650">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-651">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-652">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-652">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-653">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-653">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-654">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-654">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-655">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-655">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-656">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-656">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-657">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-657">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-658">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-658">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-659">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-659">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-660">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-660">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-661">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-661">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-662">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-662">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-663">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-663">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-664">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-664">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-665">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-665">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-666">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-666">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-667">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-667">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-668">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-668">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-669">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-669">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-670">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-670">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-671">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-671">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-672">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-672">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-673">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-673">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-674">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-674">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-675">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-675">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-676">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-676">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-677">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-677">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-678">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-678">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-679">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-680">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-680">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-682">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="13900-683">DXGI_FORMAT_R16G16B16A16 \_ unorm<sup></sup> -Fehler (11)</span><span class="sxs-lookup"><span data-stu-id="13900-683">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="13900-684">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-684">Target</span></span> | <span data-ttu-id="13900-685">Support</span><span class="sxs-lookup"><span data-stu-id="13900-685">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-686">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-687">64</span><span class="sxs-lookup"><span data-stu-id="13900-687">64</span></span> |
| <span data-ttu-id="13900-688">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-688">Format Support</span></span> | \- |
| <span data-ttu-id="13900-689">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-689">Buffer</span></span> | \- |
| <span data-ttu-id="13900-690">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-690">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-691">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-691">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-692">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-692">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-693">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-693">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-694">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-695">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-696">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-696">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-697">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-697">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-698">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-698">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-699">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-700">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-701">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-701">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-702">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-703">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-703">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-704">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-704">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-705">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-705">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-706">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-706">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-707">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-707">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-708">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-708">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-709">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-709">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-710">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-710">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-711">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-711">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-712">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-712">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-713">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-713">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-714">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-714">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-715">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-715">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-716">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-716">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-717">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-717">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-718">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-718">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-719">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-719">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-720">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-720">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-721">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-721">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-722">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-722">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-723">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-723">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-724">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-724">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-725">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-725">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-726">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-726">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-727">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-727">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-728">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-728">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-729">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-729">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-730">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-730">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-731">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-731">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-732">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-732">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="13900-733">DXGI_FORMAT_R16G16B16A16 \_ uint<sup></sup> -Benutzerkonten (12)</span><span class="sxs-lookup"><span data-stu-id="13900-733">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="13900-734">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-734">Target</span></span> | <span data-ttu-id="13900-735">Support</span><span class="sxs-lookup"><span data-stu-id="13900-735">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-736">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-736">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-737">64</span><span class="sxs-lookup"><span data-stu-id="13900-737">64</span></span> |
| <span data-ttu-id="13900-738">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-738">Format Support</span></span> | \- |
| <span data-ttu-id="13900-739">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-739">Buffer</span></span> | \- |
| <span data-ttu-id="13900-740">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-741">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-742">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-743">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-744">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-744">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-745">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-745">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-746">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-746">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-747">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-747">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-748">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-748">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-749">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-749">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-750">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-750">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-751">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-751">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-752">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-752">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-753">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-753">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-754">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-754">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-755">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-755">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-756">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-756">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-757">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-757">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-758">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-758">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-759">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-759">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-760">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-760">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-761">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-761">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-762">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-762">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-763">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-763">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-764">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-764">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-765">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-765">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-766">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-766">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-767">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-767">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-768">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-768">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-769">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-769">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-770">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-770">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-771">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-771">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-772">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-772">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-773">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-773">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-774">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-774">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-775">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-775">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-776">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-776">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-777">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-777">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-778">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-778">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-779">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-779">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-780">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-780">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-781">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-781">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-782">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="13900-783">DXGI_FORMAT_R16G16B16A16 \_ snorm<sup></sup> -Kenn Wort (13)</span><span class="sxs-lookup"><span data-stu-id="13900-783">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="13900-784">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-784">Target</span></span> | <span data-ttu-id="13900-785">Support</span><span class="sxs-lookup"><span data-stu-id="13900-785">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-786">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-787">64</span><span class="sxs-lookup"><span data-stu-id="13900-787">64</span></span> |
| <span data-ttu-id="13900-788">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-788">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-790">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-790">Buffer</span></span> | \- |
| <span data-ttu-id="13900-791">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-791">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-793">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-793">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-794">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-794">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-795">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-795">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-796">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-796">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-797">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-798">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-799">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-799">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-800">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-800">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-801">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-801">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-802">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-802">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-803">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-803">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-804">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-804">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-805">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-805">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-806">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-807">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-808">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-809">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-810">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-811">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-812">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-813">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-813">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-814">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-815">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-816">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-817">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-818">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-818">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-819">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-820">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-821">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-822">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-822">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-823">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-823">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-824">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-824">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-825">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-825">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-826">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-826">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-827">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-827">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-828">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-828">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-829">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-829">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-830">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-830">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-831">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-831">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-832">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-832">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-833">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-833">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-834">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-834">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="13900-835">DXGI_FORMAT_R16G16B16A16 \_ Sint<sup></sup> -nach SPT (14)</span><span class="sxs-lookup"><span data-stu-id="13900-835">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="13900-836">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-836">Target</span></span> | <span data-ttu-id="13900-837">Support</span><span class="sxs-lookup"><span data-stu-id="13900-837">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-838">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-838">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-839">64</span><span class="sxs-lookup"><span data-stu-id="13900-839">64</span></span> |
| <span data-ttu-id="13900-840">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-840">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-842">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-842">Buffer</span></span> | \- |
| <span data-ttu-id="13900-843">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-843">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-845">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-845">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-846">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-846">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-847">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-847">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-848">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-848">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-849">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-849">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-850">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-850">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-851">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-851">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-852">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-852">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-853">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-853">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-854">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-854">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-855">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-855">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-856">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-856">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-857">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-857">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-858">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-858">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-859">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-859">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-860">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-860">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-861">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-861">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-862">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-862">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-863">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-863">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-864">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-864">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-865">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-865">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-866">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-866">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-867">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-867">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-868">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-868">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-869">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-869">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-870">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-870">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-871">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-871">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-872">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-872">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-873">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-873">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-874">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-874">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-875">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-875">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-876">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-876">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-877">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-877">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-878">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-878">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-879">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-879">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-880">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-880">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-881">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-882">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-883">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-883">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-884">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-884">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-885">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-885">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-886">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-886">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="13900-887">DXGI_FORMAT_R32G32 \_ Typen losen<sup>PCs</sup> (15)</span><span class="sxs-lookup"><span data-stu-id="13900-887">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="13900-888">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-888">Target</span></span> | <span data-ttu-id="13900-889">Support</span><span class="sxs-lookup"><span data-stu-id="13900-889">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-890">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-891">64</span><span class="sxs-lookup"><span data-stu-id="13900-891">64</span></span> |
| <span data-ttu-id="13900-892">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-892">Format Support</span></span> | \- |
| <span data-ttu-id="13900-893">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-893">Buffer</span></span> | \- |
| <span data-ttu-id="13900-894">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-894">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-895">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-895">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-896">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-896">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-897">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-897">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-898">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-898">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-899">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-899">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-900">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-901">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-901">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-902">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-902">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-903">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-904">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-905">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-905">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-906">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-907">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-907">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-908">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-908">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-909">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-910">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-910">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-911">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-912">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-913">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-914">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-915">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-915">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-916">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-917">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-918">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-919">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-920">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-920">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-921">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-922">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-923">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-924">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-924">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-925">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-925">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-926">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-926">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-927">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-927">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-928">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-928">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-929">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-929">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-930">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-930">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-931">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-931">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-932">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-933">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-934">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-935">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-935">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-936">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-936">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="13900-937">DXGI_FORMAT_R32G32 \_ float<sup></sup> -Datentyp (16)</span><span class="sxs-lookup"><span data-stu-id="13900-937">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="13900-938">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-938">Target</span></span> | <span data-ttu-id="13900-939">Support</span><span class="sxs-lookup"><span data-stu-id="13900-939">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-940">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-940">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-941">64</span><span class="sxs-lookup"><span data-stu-id="13900-941">64</span></span> |
| <span data-ttu-id="13900-942">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-942">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-944">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-944">Buffer</span></span> | \- |
| <span data-ttu-id="13900-945">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-945">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-947">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-948">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-949">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-950">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-951">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-951">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-952">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-953">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-953">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-954">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-954">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-955">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-955">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-956">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-956">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-957">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-957">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-958">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-958">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-959">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-959">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-960">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-961">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-962">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-962">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-963">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-963">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-964">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-964">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-965">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-965">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-966">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-966">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-967">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-967">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-968">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-968">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-969">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-969">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-970">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-970">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-971">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-971">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-972">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-972">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-973">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-973">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-974">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-974">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-975">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-975">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-976">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-976">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-977">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-977">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-978">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-978">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-979">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-979">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-980">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-980">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-981">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-981">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-982">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-982">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-983">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-983">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-984">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-984">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-985">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-985">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-986">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-986">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-987">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-987">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-988">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-988">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="13900-989">DXGI_FORMAT_R32G32 \_ uint<sup></sup> -(17)</span><span class="sxs-lookup"><span data-stu-id="13900-989">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="13900-990">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-990">Target</span></span> | <span data-ttu-id="13900-991">Support</span><span class="sxs-lookup"><span data-stu-id="13900-991">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-992">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-992">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-993">64</span><span class="sxs-lookup"><span data-stu-id="13900-993">64</span></span> |
| <span data-ttu-id="13900-994">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-994">Format Support</span></span> | \- |
| <span data-ttu-id="13900-995">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-995">Buffer</span></span> | \- |
| <span data-ttu-id="13900-996">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-996">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-997">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-997">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-998">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-998">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-999">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-999">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1000">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1001">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1001">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1002">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1002">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1003">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1003">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1004">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1004">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1005">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1005">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1006">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1006">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1007">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1007">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1008">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1008">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1009">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1009">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1010">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1010">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1011">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1012">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1012">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1013">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1013">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1014">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1014">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1015">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1015">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1016">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1016">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1017">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1017">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1018">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1018">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1019">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1019">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1020">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1020">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1021">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1021">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1022">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1022">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1023">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1023">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1024">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1024">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1025">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1025">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1026">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1026">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1027">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1027">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1028">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1028">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1029">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1029">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1030">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1030">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1031">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1031">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1032">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1032">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1033">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1033">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1034">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1034">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1035">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1035">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1036">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1036">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1037">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1037">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1038">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1038">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="13900-1039">DXGI_FORMAT_R32G32 \_ Sint<sup></sup> (18)</span><span class="sxs-lookup"><span data-stu-id="13900-1039">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="13900-1040">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1040">Target</span></span> | <span data-ttu-id="13900-1041">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1041">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1042">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1042">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1043">64</span><span class="sxs-lookup"><span data-stu-id="13900-1043">64</span></span> |
| <span data-ttu-id="13900-1044">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1044">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1045">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1045">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1046">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1046">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1047">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1047">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1048">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1048">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1049">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1049">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1050">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1050">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1051">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1051">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1052">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1053">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1053">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1054">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1054">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1055">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1055">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1056">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1056">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1057">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1057">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1058">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1058">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1059">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1059">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1060">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1060">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1061">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1061">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1062">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1062">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1063">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1063">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1064">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1064">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1065">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1065">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1066">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1066">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1067">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1067">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1068">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1068">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1069">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1069">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1070">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1070">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1071">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1071">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1072">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1072">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1073">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1073">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1074">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1074">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1075">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1075">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1076">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1076">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1077">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1078">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1079">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1080">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1081">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1081">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1082">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1083">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1084">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1084">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1085">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1085">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1086">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1086">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1087">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1087">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1088">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1088">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="13900-1089">DXGI_FORMAT_R32G8X24 \_ Typen losen<sup>PCs</sup> (19)</span><span class="sxs-lookup"><span data-stu-id="13900-1089">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="13900-1090">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1090">Target</span></span> | <span data-ttu-id="13900-1091">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1091">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1092">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1093">64</span><span class="sxs-lookup"><span data-stu-id="13900-1093">64</span></span> |
| <span data-ttu-id="13900-1094">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1094">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1095">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1095">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1096">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1096">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1097">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1097">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1098">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1098">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1099">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1099">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1100">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1100">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1101">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1101">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1102">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1102">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1103">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1103">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1104">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1105">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1106">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1107">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1107">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1108">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1109">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1109">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1110">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1110">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1111">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1112">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1113">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1114">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1115">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1116">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1117">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1117">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1118">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1119">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1120">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1121">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1122">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1123">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1124">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1124">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1125">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1125">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1126">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1126">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1127">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1127">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1128">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1128">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1129">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1129">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1130">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1130">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1131">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1131">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1132">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1132">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1133">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1133">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1134">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1134">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1135">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1135">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1136">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1136">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1137">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1137">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1138">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1138">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="13900-1139">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup></sup> -(20)</span><span class="sxs-lookup"><span data-stu-id="13900-1139">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="13900-1140">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1140">Target</span></span> | <span data-ttu-id="13900-1141">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1141">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1142">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1142">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1143">64</span><span class="sxs-lookup"><span data-stu-id="13900-1143">64</span></span> |
| <span data-ttu-id="13900-1144">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1144">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1145">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1145">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1146">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1146">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1147">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1147">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1148">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1148">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1149">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1149">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1150">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1151">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1151">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1152">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1152">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1153">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1153">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1154">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1154">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1155">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1155">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1156">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1156">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1157">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1157">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1158">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1158">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1159">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1159">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1160">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1160">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1161">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1161">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1162">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1163">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1164">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1165">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1166">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1167">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1167">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1168">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1168">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1169">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1169">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1170">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1170">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1171">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1171">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1172">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1172">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1173">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1173">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1174">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1174">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1175">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1175">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1176">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1176">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1177">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1178">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1179">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1180">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1181">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1181">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1182">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1183">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1184">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1184">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1185">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1185">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1186">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1186">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1187">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1187">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1188">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1188">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="13900-1189">DXGI_FORMAT_R32 \_ float \_ X8X24 \_ typlose<sup></sup> Rechtschreibfehler (21)</span><span class="sxs-lookup"><span data-stu-id="13900-1189">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="13900-1190">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1190">Target</span></span> | <span data-ttu-id="13900-1191">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1191">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1192">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1192">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1193">64</span><span class="sxs-lookup"><span data-stu-id="13900-1193">64</span></span> |
| <span data-ttu-id="13900-1194">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1194">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1195">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1195">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1196">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1196">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1197">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1197">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1198">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1198">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1199">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1199">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1200">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1200">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1201">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1201">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1202">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1202">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1203">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1203">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1204">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1204">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1205">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1205">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1206">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1206">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1207">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1207">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1208">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1208">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1209">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1209">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1210">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1210">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1211">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1211">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1212">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1212">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1213">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1213">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1214">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1214">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1215">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1215">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1216">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1216">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1217">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1217">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1218">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1218">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1219">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1219">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1220">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1220">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1221">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1221">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1222">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1222">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1223">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1223">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1224">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1224">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1225">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1225">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1226">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1226">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1227">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1227">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1228">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1228">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1229">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1229">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1230">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1230">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1231">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1231">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1232">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1232">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1233">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1233">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1234">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1235">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1236">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1237">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1237">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1238">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1238">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="13900-1239">DXGI_FORMAT_X32 \_ typlose \_ G8X24 \_ uint<sup></sup> -Fehler (22)</span><span class="sxs-lookup"><span data-stu-id="13900-1239">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="13900-1240">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1240">Target</span></span> | <span data-ttu-id="13900-1241">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1241">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1242">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1242">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1243">64</span><span class="sxs-lookup"><span data-stu-id="13900-1243">64</span></span> |
| <span data-ttu-id="13900-1244">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1244">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1245">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1245">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1246">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1246">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1247">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1247">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1248">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1248">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1249">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1249">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1250">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1250">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1251">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1252">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1253">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1253">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1254">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1254">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1255">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1256">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1257">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1257">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1258">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1259">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1259">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1260">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1260">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1261">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1261">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1262">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1262">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1263">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1263">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1264">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1264">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1265">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1265">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1266">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1266">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1267">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1267">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1268">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1268">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1269">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1269">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1270">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1270">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1271">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1271">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1272">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1272">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1273">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1273">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1274">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1274">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1275">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1275">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1276">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1276">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1277">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1277">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1278">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1278">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1279">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1279">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1280">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1280">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1281">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1281">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1282">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1283">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1283">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1284">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1284">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1285">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1285">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1286">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1286">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1287">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1287">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1288">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1288">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="13900-1289">DXGI_FORMAT_R10G10B10A2 \_ typlosen<sup>PCs</sup> (23)</span><span class="sxs-lookup"><span data-stu-id="13900-1289">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="13900-1290">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1290">Target</span></span> | <span data-ttu-id="13900-1291">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1291">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1292">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1292">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1293">32</span><span class="sxs-lookup"><span data-stu-id="13900-1293">32</span></span> |
| <span data-ttu-id="13900-1294">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1294">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1295">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1295">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1296">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1296">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1297">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1298">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1299">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1300">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1301">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1301">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1302">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1302">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1303">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1303">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1304">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1304">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1305">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1305">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1306">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1306">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1307">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1307">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1308">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1308">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1309">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1309">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1310">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1310">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1311">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1311">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1312">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1312">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1313">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1313">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1314">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1314">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1315">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1315">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1316">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1316">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1317">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1317">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1318">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1318">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1319">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1319">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1320">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1320">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1321">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1321">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1322">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1322">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1323">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1323">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1324">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1324">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1325">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1325">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1326">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1326">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1327">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1327">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1328">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1328">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1329">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1329">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1330">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1330">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1331">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1331">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1332">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1332">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1333">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1333">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1334">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1334">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1335">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1335">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1336">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1336">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1337">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1337">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1338">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1338">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="13900-1339">DXGI_FORMAT_R10G10B10A2 \_ unorm<sup></sup> -Fehler (24)</span><span class="sxs-lookup"><span data-stu-id="13900-1339">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="13900-1340">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1340">Target</span></span> | <span data-ttu-id="13900-1341">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1341">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1342">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1342">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1343">32</span><span class="sxs-lookup"><span data-stu-id="13900-1343">32</span></span> |
| <span data-ttu-id="13900-1344">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1344">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1345">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1345">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1346">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1346">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1347">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1348">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1349">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1350">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1350">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1351">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1351">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1352">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1352">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1353">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1353">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1354">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1354">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1355">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1355">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1356">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1356">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1357">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1357">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1358">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1358">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1359">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1359">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1360">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1360">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1361">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1361">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1362">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1362">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1363">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1363">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1364">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1364">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1365">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1365">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1366">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1366">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1367">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1367">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1368">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1368">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1369">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1369">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1370">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1370">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1371">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1371">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1372">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1372">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1373">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1373">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1374">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1374">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1375">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1375">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1376">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1376">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1377">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1377">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1378">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1378">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1379">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1379">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1380">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1380">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1381">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1381">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1382">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1382">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1383">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1383">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1384">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1385">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1386">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1387">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1387">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1389">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="13900-1390">DXGI_FORMAT_R10G10B10A2 \_ uint<sup></sup> -(25)</span><span class="sxs-lookup"><span data-stu-id="13900-1390">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="13900-1391">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1391">Target</span></span> | <span data-ttu-id="13900-1392">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1392">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1393">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1394">32</span><span class="sxs-lookup"><span data-stu-id="13900-1394">32</span></span> |
| <span data-ttu-id="13900-1395">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1395">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1396">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1396">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1397">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1397">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1398">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1398">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1399">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1399">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1400">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1400">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1401">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1401">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1402">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1402">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1403">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1403">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1404">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1404">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1405">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1405">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1406">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1406">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1407">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1407">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1408">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1408">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1409">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1409">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1410">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1410">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1411">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1411">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1412">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1413">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1413">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1414">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1414">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1415">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1415">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1416">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1416">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1417">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1417">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1418">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1418">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1419">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1419">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1420">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1420">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1421">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1421">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1422">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1422">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1423">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1423">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1424">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1424">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1425">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1425">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1426">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1426">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1427">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1427">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1428">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1429">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1430">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1431">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1432">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1432">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1433">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1434">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1435">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1435">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1436">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1436">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1437">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1437">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1438">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1438">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1439">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1439">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="13900-1440">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ unorm<sup></sup> -Fehler (89)</span><span class="sxs-lookup"><span data-stu-id="13900-1440">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="13900-1441">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1441">Target</span></span> | <span data-ttu-id="13900-1442">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1442">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1443">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1443">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1444">32</span><span class="sxs-lookup"><span data-stu-id="13900-1444">32</span></span> |
| <span data-ttu-id="13900-1445">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1445">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1446">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1446">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1447">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1447">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1448">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1448">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1449">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1449">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1450">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1450">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1451">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1451">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1453">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1454">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1454">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1455">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1456">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1457">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1458">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1459">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1460">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1460">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1461">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1461">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1462">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1462">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1463">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1463">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1464">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1465">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1466">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1467">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1468">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1468">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1469">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1470">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1471">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1472">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1474">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1475">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1476">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1477">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1477">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1478">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1478">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1479">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1479">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1480">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1481">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1482">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1482">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1483">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1484">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1485">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1486">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1487">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1488">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1488">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1489">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="13900-1490">DXGI_FORMAT_R11G11B10 \_ float<sup></sup> -Datentyp (26)</span><span class="sxs-lookup"><span data-stu-id="13900-1490">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="13900-1491">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1491">Target</span></span> | <span data-ttu-id="13900-1492">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1492">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1493">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1494">32</span><span class="sxs-lookup"><span data-stu-id="13900-1494">32</span></span> |
| <span data-ttu-id="13900-1495">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1495">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1496">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1496">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1497">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1498">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1499">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1500">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1501">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1502">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1503">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1504">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1505">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1506">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1507">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1508">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1508">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1509">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1510">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1510">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1511">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1512">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1513">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1514">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1515">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1516">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1517">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1518">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1518">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1519">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1520">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1521">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1522">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1523">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1524">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1525">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1526">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1527">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1528">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1528">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1529">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1529">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1530">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1530">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1531">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1531">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1532">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1532">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1533">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1533">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1534">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1534">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1535">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1535">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1536">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1536">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1537">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1537">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1538">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1538">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1539">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1539">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="13900-1540">DXGI_FORMAT_R8G8B8A8 \_ typlosen<sup>PCs</sup> (27)</span><span class="sxs-lookup"><span data-stu-id="13900-1540">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="13900-1541">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1541">Target</span></span> | <span data-ttu-id="13900-1542">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1542">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1543">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1543">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1544">32</span><span class="sxs-lookup"><span data-stu-id="13900-1544">32</span></span> |
| <span data-ttu-id="13900-1545">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1545">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1546">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1546">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1547">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1548">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1549">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1550">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1551">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1552">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1552">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1553">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1553">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1554">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1554">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1555">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1555">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1556">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1556">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1557">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1557">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1558">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1558">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1559">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1559">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1560">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1560">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1561">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1561">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1562">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1562">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1563">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1563">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1564">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1565">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1566">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1567">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1568">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1568">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1569">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1570">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1571">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1572">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1573">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1573">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1574">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1575">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1576">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1577">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1577">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1578">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1578">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1579">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1579">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1580">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1580">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1581">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1581">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1582">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1582">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1583">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1583">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1584">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1584">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1585">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1585">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1586">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1586">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1587">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1587">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1588">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1588">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1589">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="13900-1590">DXGI_FORMAT_R8G8B8A8 \_ unorm<sup></sup> -Fehler (28)</span><span class="sxs-lookup"><span data-stu-id="13900-1590">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="13900-1591">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1591">Target</span></span> | <span data-ttu-id="13900-1592">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1592">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1593">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1594">32</span><span class="sxs-lookup"><span data-stu-id="13900-1594">32</span></span> |
| <span data-ttu-id="13900-1595">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1595">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1597">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1597">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1598">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1598">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1600">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1601">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1603">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1605">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1605">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1607">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1609">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1609">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1611">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1611">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1613">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1614">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1615">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1615">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1616">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1617">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1617">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1619">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1619">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1621">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1621">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1623">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1623">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1625">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1625">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1626">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1626">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1627">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1627">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1628">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1628">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1629">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1629">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1630">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1630">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1631">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1631">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1632">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1632">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1633">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1633">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1634">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1634">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1635">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1635">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1636">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1636">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1637">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1637">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1638">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1638">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1640">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1640">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-1642">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1642">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-1644">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1644">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-1646">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1646">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1648">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1648">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1649">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1649">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1651">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1651">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1652">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1652">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1653">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1653">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-1655">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1655">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1657">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1657">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1659">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1659">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="13900-1660">DXGI_FORMAT_R8G8B8A8 \_ unorm \_ sRGB<sup></sup> -Fehler (29)</span><span class="sxs-lookup"><span data-stu-id="13900-1660">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="13900-1661">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1661">Target</span></span> | <span data-ttu-id="13900-1662">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1662">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1663">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1663">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1664">32</span><span class="sxs-lookup"><span data-stu-id="13900-1664">32</span></span> |
| <span data-ttu-id="13900-1665">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1665">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1667">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1667">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1668">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1668">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1669">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1669">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1670">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1670">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1671">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1671">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1672">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1672">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1674">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1674">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1676">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1676">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1678">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1678">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1680">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1680">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1682">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1682">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1683">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1683">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1684">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1684">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1685">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1685">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1686">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1686">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1688">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1688">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1690">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1690">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1692">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1692">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1694">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1694">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1695">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1695">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1696">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1696">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1697">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1697">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1698">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1698">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1699">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1699">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1700">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1700">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1701">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1701">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1702">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1702">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1703">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1703">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1704">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1704">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1705">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1705">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1706">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1706">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1707">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1707">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1709">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1709">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-1711">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1711">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-1713">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1713">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-1715">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1715">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1717">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1717">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1718">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1718">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1720">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1720">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1721">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1721">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1722">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1722">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-1724">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1724">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1726">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1726">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1728">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1728">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="13900-1729">DXGI_FORMAT_R8G8B8A8 \_ uint<sup></sup> -(30)</span><span class="sxs-lookup"><span data-stu-id="13900-1729">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="13900-1730">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1730">Target</span></span> | <span data-ttu-id="13900-1731">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1731">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1732">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1732">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1733">32</span><span class="sxs-lookup"><span data-stu-id="13900-1733">32</span></span> |
| <span data-ttu-id="13900-1734">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1734">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1736">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1736">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1737">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1737">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1739">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1739">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1740">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1740">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1741">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1741">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1742">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1742">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1743">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1743">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1744">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1744">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1745">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1745">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1746">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1746">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1747">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1748">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1749">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1749">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1750">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1750">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1751">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1751">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1752">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1752">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1753">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1753">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1754">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1754">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1755">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1755">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1756">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1756">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1757">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1757">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1758">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1758">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1759">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1759">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1760">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1760">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1761">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1761">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1762">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1762">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1763">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1763">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1764">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1764">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1765">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1765">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1766">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1766">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1767">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1767">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1768">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1768">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1769">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1770">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1771">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1772">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1773">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1773">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1774">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1775">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1775">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1776">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1777">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1778">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1779">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1779">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1780">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="13900-1781">\_Snorm-<sup></sup> snorm (31) DXGI_FORMAT_R8G8B8A8</span><span class="sxs-lookup"><span data-stu-id="13900-1781">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="13900-1782">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1782">Target</span></span> | <span data-ttu-id="13900-1783">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1784">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1785">32</span><span class="sxs-lookup"><span data-stu-id="13900-1785">32</span></span> |
| <span data-ttu-id="13900-1786">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1786">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1788">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1789">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1789">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1790">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1790">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1791">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1791">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1792">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1792">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1793">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1793">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1796">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1798">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1798">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1800">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1800">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1802">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1803">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1804">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1804">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1805">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1806">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1806">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1808">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1809">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1810">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1811">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1812">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1813">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1814">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1815">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1815">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1816">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1816">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1817">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1817">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1818">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1818">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1819">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1819">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1820">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1820">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1821">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1821">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1822">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1822">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1823">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1823">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1824">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1824">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-1826">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1826">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1827">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1827">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1828">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1828">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1829">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1829">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1830">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1830">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1831">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1831">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1832">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1832">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1833">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1833">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1834">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1834">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1835">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1835">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1836">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1836">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1837">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="13900-1838">DXGI_FORMAT_R8G8B8A8 \_ Sint<sup></sup> -SPT (32)</span><span class="sxs-lookup"><span data-stu-id="13900-1838">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="13900-1839">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1839">Target</span></span> | <span data-ttu-id="13900-1840">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1840">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1841">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1842">32</span><span class="sxs-lookup"><span data-stu-id="13900-1842">32</span></span> |
| <span data-ttu-id="13900-1843">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1843">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1844">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1844">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1845">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1845">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1846">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1846">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1847">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1847">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1848">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1848">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1849">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1849">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1850">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1850">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1851">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1851">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1852">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1852">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1853">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1853">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1854">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1855">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1856">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1857">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1858">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1858">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1859">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1859">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1860">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1860">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1861">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1861">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1862">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1862">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1863">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1863">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1864">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1864">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1865">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1865">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1866">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1866">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1867">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1867">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1868">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1868">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1869">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1869">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1870">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1870">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1871">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1871">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1872">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1872">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1873">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1873">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1874">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1874">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1875">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1875">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1876">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1876">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1877">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1877">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1878">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1878">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1879">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1879">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1880">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1880">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1881">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1881">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1882">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1882">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1883">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1883">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1884">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1884">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1885">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1885">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1886">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1886">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1887">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1887">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="13900-1888">DXGI_FORMAT_R16G16 \_ Typen losen<sup>PCs</sup> (33)</span><span class="sxs-lookup"><span data-stu-id="13900-1888">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="13900-1889">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1889">Target</span></span> | <span data-ttu-id="13900-1890">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1890">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1891">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1891">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1892">32</span><span class="sxs-lookup"><span data-stu-id="13900-1892">32</span></span> |
| <span data-ttu-id="13900-1893">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1893">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1894">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1894">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1895">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1896">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1897">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1898">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1899">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1899">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1900">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1900">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1901">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1901">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1902">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1902">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1903">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1903">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1904">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1904">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1905">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1905">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1906">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1906">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1907">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1907">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1908">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1908">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1909">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1909">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1910">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1910">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1911">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1911">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1912">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1912">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1913">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1913">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1914">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1914">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1915">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1915">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1916">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1916">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1917">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1917">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1918">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1918">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1919">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1919">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1920">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1920">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1921">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1921">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1922">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1922">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1923">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1923">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1924">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1924">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1925">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1925">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1926">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1926">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1927">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1927">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1928">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1928">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1929">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1929">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1930">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1930">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1931">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1931">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1932">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1932">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1933">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1933">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1934">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1934">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1935">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1935">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1936">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1936">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1937">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="13900-1938">DXGI_FORMAT_R16G16 \_ float-"<sup>f</sup> " (34)</span><span class="sxs-lookup"><span data-stu-id="13900-1938">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="13900-1939">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1939">Target</span></span> | <span data-ttu-id="13900-1940">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1940">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1941">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1942">32</span><span class="sxs-lookup"><span data-stu-id="13900-1942">32</span></span> |
| <span data-ttu-id="13900-1943">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1943">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1944">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1944">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1945">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1945">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1946">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1946">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1947">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1947">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1948">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1948">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1949">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1949">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-1950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-1950">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-1951">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-1951">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-1952">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-1952">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-1953">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-1954">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-1955">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-1955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-1956">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-1956">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-1957">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-1957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-1958">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1958">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-1959">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-1959">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-1960">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1960">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1961">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1961">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1962">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-1962">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-1963">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1963">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-1964">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1964">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1965">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-1965">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-1966">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-1966">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-1967">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-1967">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-1968">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1968">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-1969">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-1969">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-1970">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-1970">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-1971">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-1971">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-1972">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-1972">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-1973">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-1973">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1974">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-1974">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-1975">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-1975">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-1976">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1976">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1977">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-1977">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-1978">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-1978">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-1979">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-1979">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-1980">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-1980">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-1981">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-1981">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-1982">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-1982">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-1983">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-1983">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-1984">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1984">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-1985">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-1985">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-1986">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1986">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-1987">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-1987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="13900-1988">DXGI_FORMAT_R16G16 \_ unorm<sup></sup> -Fehler (35)</span><span class="sxs-lookup"><span data-stu-id="13900-1988">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="13900-1989">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-1989">Target</span></span> | <span data-ttu-id="13900-1990">Support</span><span class="sxs-lookup"><span data-stu-id="13900-1990">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-1991">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-1991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-1992">32</span><span class="sxs-lookup"><span data-stu-id="13900-1992">32</span></span> |
| <span data-ttu-id="13900-1993">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-1993">Format Support</span></span> | \- |
| <span data-ttu-id="13900-1994">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-1994">Buffer</span></span> | \- |
| <span data-ttu-id="13900-1995">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-1995">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-1996">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-1996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-1997">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-1997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-1998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-1998">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-1999">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-1999">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2000">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2000">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2001">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2001">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2002">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2002">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2003">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2003">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2004">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2004">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2005">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2005">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2006">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2006">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2007">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2007">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2008">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2008">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2009">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2009">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2010">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2010">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2011">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2011">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2012">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2013">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2014">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2015">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2016">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2016">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2017">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2018">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2019">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2020">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2021">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2022">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2023">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2023">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2024">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2024">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2025">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2025">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2026">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2026">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2027">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2027">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2028">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2028">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2029">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2029">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2030">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2030">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2031">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2031">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2032">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2032">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2033">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2033">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2034">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2034">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2035">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2035">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2036">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2036">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2037">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2037">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="13900-2038">DXGI_FORMAT_R16G16 \_ uint<sup></sup> -Benutzerkonten (36)</span><span class="sxs-lookup"><span data-stu-id="13900-2038">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="13900-2039">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2039">Target</span></span> | <span data-ttu-id="13900-2040">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2040">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2041">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2041">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2042">32</span><span class="sxs-lookup"><span data-stu-id="13900-2042">32</span></span> |
| <span data-ttu-id="13900-2043">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2043">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2044">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2044">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2045">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2045">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2046">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2046">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2047">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2047">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2048">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2048">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2049">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2049">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2050">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2051">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2052">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2053">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2054">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2055">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2056">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2056">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2057">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2058">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2058">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2059">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2060">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2061">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2062">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2063">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2064">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2065">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2066">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2066">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2067">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2068">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2069">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2070">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2071">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2072">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2073">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2074">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2075">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2075">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2076">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2076">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2077">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2077">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2078">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2078">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2079">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2079">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2080">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2080">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2081">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2081">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2082">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2082">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2083">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2083">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2084">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2084">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2085">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2085">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2086">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2086">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2087">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2087">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="13900-2088">DXGI_FORMAT_R16G16 \_ snorm<sup></sup> -Kenn Wort (37)</span><span class="sxs-lookup"><span data-stu-id="13900-2088">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="13900-2089">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2089">Target</span></span> | <span data-ttu-id="13900-2090">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2090">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2091">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2091">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2092">32</span><span class="sxs-lookup"><span data-stu-id="13900-2092">32</span></span> |
| <span data-ttu-id="13900-2093">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2093">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2095">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2095">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2096">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2096">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2098">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2098">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2099">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2099">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2100">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2100">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2101">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2101">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2103">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2104">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2105">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2105">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2107">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2107">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2108">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2108">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2109">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2109">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2110">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2110">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2111">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2111">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2112">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2112">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2114">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2114">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2115">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2115">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2116">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2116">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2117">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2117">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2118">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2118">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2119">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2119">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2120">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2120">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2121">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2121">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2122">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2122">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2123">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2123">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2124">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2124">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2125">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2125">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2126">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2126">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2127">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2127">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2128">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2128">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2129">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2129">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2130">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2130">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2132">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2132">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2133">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2133">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2134">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2134">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2135">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2135">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2136">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2136">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2137">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2137">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2138">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2138">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2139">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2139">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2140">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2140">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2141">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2141">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2142">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2142">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2143">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2143">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="13900-2144">DXGI_FORMAT_R16G16 \_ Sint<sup></sup> -SPT (38)</span><span class="sxs-lookup"><span data-stu-id="13900-2144">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="13900-2145">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2145">Target</span></span> | <span data-ttu-id="13900-2146">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2146">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2147">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2148">32</span><span class="sxs-lookup"><span data-stu-id="13900-2148">32</span></span> |
| <span data-ttu-id="13900-2149">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2149">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2151">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2151">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2152">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2152">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2154">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2154">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2155">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2155">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2156">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2156">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2157">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2157">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2158">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2158">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2159">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2159">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2160">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2160">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2161">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2162">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2163">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2164">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2164">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2165">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2166">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2166">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2167">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2167">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2168">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2168">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2169">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2169">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2170">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2170">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2171">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2171">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2172">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2172">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2173">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2173">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2174">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2174">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2175">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2175">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2176">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2176">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2177">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2177">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2178">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2178">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2179">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2179">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2180">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2180">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2181">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2181">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2182">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2182">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2183">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2183">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2184">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2185">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2186">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2187">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2188">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2188">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2189">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2190">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2191">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2191">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2192">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2192">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2193">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2193">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2194">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2194">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2195">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="13900-2196">DXGI_FORMAT_R32 \_ Typen losen<sup>PCs</sup> (39)</span><span class="sxs-lookup"><span data-stu-id="13900-2196">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="13900-2197">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2197">Target</span></span> | <span data-ttu-id="13900-2198">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2198">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2199">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2200">32</span><span class="sxs-lookup"><span data-stu-id="13900-2200">32</span></span> |
| <span data-ttu-id="13900-2201">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2201">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2202">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2202">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2203">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2204">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2205">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2206">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2207">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2208">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2209">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2209">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2210">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2210">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2211">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2211">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2212">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2212">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2213">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2213">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2214">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2214">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2215">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2215">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2216">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2216">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2217">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2217">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2218">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2218">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2219">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2219">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2220">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2220">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2221">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2221">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2222">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2222">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2223">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2223">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2224">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2224">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2225">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2225">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2226">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2226">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2227">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2227">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2228">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2228">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2229">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2229">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2230">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2230">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2231">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2231">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2232">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2232">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2233">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2233">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2234">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2234">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2235">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2235">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2236">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2236">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2237">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2237">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2238">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2238">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2239">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2239">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2240">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2240">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2241">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2241">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2242">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2242">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2243">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2243">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2244">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2244">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2245">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2245">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="13900-2246">DXGI_FORMAT_D32 \_ float-"<sup>f</sup> " (40)</span><span class="sxs-lookup"><span data-stu-id="13900-2246">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="13900-2247">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2247">Target</span></span> | <span data-ttu-id="13900-2248">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2248">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2249">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2249">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2250">32</span><span class="sxs-lookup"><span data-stu-id="13900-2250">32</span></span> |
| <span data-ttu-id="13900-2251">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2251">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2252">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2252">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2253">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2253">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2254">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2254">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2255">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2255">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2256">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2256">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2257">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2258">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2258">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2259">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2259">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2260">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2260">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2261">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2261">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2262">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2262">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2263">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2263">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2264">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2264">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2265">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2265">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2266">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2266">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2267">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2267">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2268">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2268">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2269">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2269">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2270">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2270">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2271">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2271">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2272">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2272">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2273">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2273">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2274">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2274">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2275">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2275">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2276">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2276">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2277">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2277">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2278">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2278">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2279">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2279">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2280">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2280">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2281">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2281">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2282">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2282">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2283">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2283">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2284">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2284">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2285">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2285">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2286">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2286">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2287">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2287">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2288">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2288">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2289">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2289">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2290">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2290">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2291">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2291">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2292">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2292">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2293">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2293">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2294">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2294">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2295">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2295">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="13900-2296">DXGI_FORMAT_R32 \_ float-"<sup>f</sup> " (41)</span><span class="sxs-lookup"><span data-stu-id="13900-2296">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="13900-2297">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2297">Target</span></span> | <span data-ttu-id="13900-2298">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2298">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2299">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2299">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2300">32</span><span class="sxs-lookup"><span data-stu-id="13900-2300">32</span></span> |
| <span data-ttu-id="13900-2301">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2301">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2303">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2303">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2304">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2304">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2306">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2306">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2307">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2307">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2308">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2308">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2309">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2309">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2310">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2310">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2311">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2311">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2312">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2312">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2313">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2313">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2314">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2314">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2315">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2315">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2316">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2316">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2317">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2317">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2318">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2318">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2319">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2320">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2321">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2322">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2323">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2324">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2325">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2326">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2326">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2327">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2328">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2329">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2330">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2331">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2332">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2333">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2334">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2335">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2335">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2336">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2336">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2337">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2337">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2338">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2338">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2339">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2339">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2340">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2340">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2341">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2341">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2342">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2342">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2343">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2343">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2344">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2344">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2345">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2345">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2346">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2346">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2347">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2347">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="13900-2348">DXGI_FORMAT_R32 \_ uint<sup></sup> -Benutzerkonten (42)</span><span class="sxs-lookup"><span data-stu-id="13900-2348">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="13900-2349">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2349">Target</span></span> | <span data-ttu-id="13900-2350">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2350">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2351">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2351">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2352">32</span><span class="sxs-lookup"><span data-stu-id="13900-2352">32</span></span> |
| <span data-ttu-id="13900-2353">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2353">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2354">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2354">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2355">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2355">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2356">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2356">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2357">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2357">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2358">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2358">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2359">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2359">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2360">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2361">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2362">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2362">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2363">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2363">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2364">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2364">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2365">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2365">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2366">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2366">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2367">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2367">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2368">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2368">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2369">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2369">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2370">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2371">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2371">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2372">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2372">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2373">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2373">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2374">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2374">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2375">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2375">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2376">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2376">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2377">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2377">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2378">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2378">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2379">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2379">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2380">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2380">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2381">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2381">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2382">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2382">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2383">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2383">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2384">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2384">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2385">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2385">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2386">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2386">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2387">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2387">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2388">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2388">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2389">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2389">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2390">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2390">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2391">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2391">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2392">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2392">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2393">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2393">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2394">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2394">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2395">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2395">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2396">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2396">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2397">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2397">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="13900-2398">DXGI_FORMAT_R32 \_ Sint<sup></sup> -SPT (43)</span><span class="sxs-lookup"><span data-stu-id="13900-2398">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="13900-2399">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2399">Target</span></span> | <span data-ttu-id="13900-2400">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2400">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2401">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2401">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2402">32</span><span class="sxs-lookup"><span data-stu-id="13900-2402">32</span></span> |
| <span data-ttu-id="13900-2403">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2403">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2404">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2404">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2405">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2405">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2406">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2406">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2407">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2407">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2408">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2408">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2409">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2409">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2410">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2410">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2411">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2411">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2412">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2412">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2413">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2414">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2415">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2416">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2416">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2417">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2418">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2418">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2419">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2419">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2420">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2420">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2421">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2421">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2422">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2422">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2423">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2423">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2424">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2424">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2425">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2425">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2426">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2426">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2427">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2427">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2428">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2428">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2429">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2429">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2430">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2430">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2431">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2431">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2432">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2432">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2433">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2433">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2434">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2434">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2435">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2435">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2436">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2437">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2438">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2439">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2440">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2440">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2441">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2442">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2442">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2443">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2443">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2444">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2444">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2445">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2445">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2446">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2446">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2447">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2447">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="13900-2448">DXGI_FORMAT_R24G8 \_ Typen losen<sup>PCs</sup> (44)</span><span class="sxs-lookup"><span data-stu-id="13900-2448">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="13900-2449">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2449">Target</span></span> | <span data-ttu-id="13900-2450">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2450">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2451">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2451">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2452">32</span><span class="sxs-lookup"><span data-stu-id="13900-2452">32</span></span> |
| <span data-ttu-id="13900-2453">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2453">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2454">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2454">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2455">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2455">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2456">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2456">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2457">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2457">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2458">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2458">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2459">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2459">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2460">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2460">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2461">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2461">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2462">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2462">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2463">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2463">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2464">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2464">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2465">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2465">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2466">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2466">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2467">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2467">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2468">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2468">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2469">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2470">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2471">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2472">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2473">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2474">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2475">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2476">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2476">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2477">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2478">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2479">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2480">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2481">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2482">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2483">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2484">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2485">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2485">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2486">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2486">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2487">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2487">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2488">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2488">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2489">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2489">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2490">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2490">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2491">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2491">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2492">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2492">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2493">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2494">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2495">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2496">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2496">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2497">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="13900-2498">DXGI_FORMAT_D24 \_ unorm \_ S8 \_ uint<sup></sup> -Fehler (45)</span><span class="sxs-lookup"><span data-stu-id="13900-2498">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="13900-2499">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2499">Target</span></span> | <span data-ttu-id="13900-2500">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2500">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2501">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2502">32</span><span class="sxs-lookup"><span data-stu-id="13900-2502">32</span></span> |
| <span data-ttu-id="13900-2503">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2503">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2505">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2505">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2506">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2507">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2508">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2509">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2510">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2512">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2513">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2514">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2515">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2516">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2517">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2518">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2518">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2519">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2520">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2520">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2521">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2522">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2523">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2524">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2525">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2525">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2527">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2527">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2528">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2528">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2529">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2529">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2530">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2530">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2531">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2531">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2532">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2532">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2533">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2533">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2534">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2534">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2535">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2535">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2536">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2536">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2537">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2537">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2538">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2538">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2539">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2539">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-2541">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2541">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-2543">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2543">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-2545">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2545">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2546">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2546">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2547">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2547">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2548">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2548">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2549">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2549">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2550">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2550">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2551">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2551">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2552">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2552">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2553">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2553">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="13900-2554">DXGI_FORMAT_R24 \_ unorm \_ X8- \_ typlosen, nicht (46)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="13900-2554">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="13900-2555">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2555">Target</span></span> | <span data-ttu-id="13900-2556">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2556">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2557">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2557">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2558">32</span><span class="sxs-lookup"><span data-stu-id="13900-2558">32</span></span> |
| <span data-ttu-id="13900-2559">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2559">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2560">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2560">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2561">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2561">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2562">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2563">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2564">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2565">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2565">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2566">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2567">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2567">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2568">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2568">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2569">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2569">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2570">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2570">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2571">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2571">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2572">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2572">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2573">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2573">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2574">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2574">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2575">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2575">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2576">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2576">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2577">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2577">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2578">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2578">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2579">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2579">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2580">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2580">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2581">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2581">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2582">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2582">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2583">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2583">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2584">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2584">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2585">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2585">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2586">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2586">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2587">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2587">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2588">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2588">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2589">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2589">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2590">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2590">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2591">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2591">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2592">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2592">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2593">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2593">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2594">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2594">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2595">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2595">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2596">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2596">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2597">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2597">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2598">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2598">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2599">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2600">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2601">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2602">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2602">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2603">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="13900-2604">DXGI_FORMAT_X24 \_ typlose \_ G8 \_ uint<sup></sup> -Benutzerkonten (47)</span><span class="sxs-lookup"><span data-stu-id="13900-2604">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="13900-2605">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2605">Target</span></span> | <span data-ttu-id="13900-2606">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2606">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2607">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2608">32</span><span class="sxs-lookup"><span data-stu-id="13900-2608">32</span></span> |
| <span data-ttu-id="13900-2609">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2609">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2610">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2610">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2611">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2611">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2612">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2612">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2613">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2613">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2614">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2614">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2615">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2616">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2616">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2617">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2617">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2618">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2618">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2619">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2620">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2620">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2621">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2621">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2622">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2622">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2623">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2623">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2624">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2624">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2625">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2625">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2626">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2626">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2627">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2627">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2628">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2628">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2629">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2629">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2630">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2630">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2631">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2631">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2632">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2632">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2633">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2633">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2634">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2634">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2635">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2635">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2636">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2636">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2637">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2637">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2638">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2638">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2639">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2639">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2640">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2640">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2641">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2641">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2642">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2642">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2643">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2643">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2644">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2644">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2645">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2645">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2646">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2646">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2647">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2647">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2648">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2648">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2649">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2649">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2650">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2650">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2651">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2651">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2652">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2652">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2653">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2653">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="13900-2654">DXGI_FORMAT_R8G8 \_ Typen losen<sup>PCs</sup> (48)</span><span class="sxs-lookup"><span data-stu-id="13900-2654">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="13900-2655">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2655">Target</span></span> | <span data-ttu-id="13900-2656">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2656">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2657">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2657">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2658">16</span><span class="sxs-lookup"><span data-stu-id="13900-2658">16</span></span> |
| <span data-ttu-id="13900-2659">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2659">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2660">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2660">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2661">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2661">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2662">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2662">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2663">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2663">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2664">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2664">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2665">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2666">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2666">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2667">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2667">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2668">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2668">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2669">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2669">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2670">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2670">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2671">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2671">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2672">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2672">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2673">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2673">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2674">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2674">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2675">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2675">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2676">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2676">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2677">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2677">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2678">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2678">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2679">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2679">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2680">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2680">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2681">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2681">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2682">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2682">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2683">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2683">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2684">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2684">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2685">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2685">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2686">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2686">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2687">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2687">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2688">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2688">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2689">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2689">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2690">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2690">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2691">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2691">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2692">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2693">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2694">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2695">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2696">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2696">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2697">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2698">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2699">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2700">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2700">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2701">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2701">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2702">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2702">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2703">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2703">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="13900-2704">DXGI_FORMAT_R8G8 \_ unorm<sup></sup> -Fehler (49)</span><span class="sxs-lookup"><span data-stu-id="13900-2704">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="13900-2705">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2705">Target</span></span> | <span data-ttu-id="13900-2706">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2706">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2707">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2707">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2708">16</span><span class="sxs-lookup"><span data-stu-id="13900-2708">16</span></span> |
| <span data-ttu-id="13900-2709">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2709">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2711">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2711">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2712">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2712">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2713">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2713">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2714">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2714">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2715">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2715">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2716">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2718">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2719">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2719">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2720">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2720">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2722">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2722">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2724">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2724">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2725">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2725">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2726">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2726">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2727">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2727">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2728">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2728">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2729">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2729">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2730">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2730">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2732">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2732">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2734">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2734">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2735">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2735">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2736">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2736">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2737">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2737">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2738">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2738">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2739">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2739">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2740">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2740">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2741">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2741">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2742">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2742">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2743">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2743">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2744">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2744">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2745">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2745">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2746">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2746">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2747">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2747">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2749">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2749">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2750">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2750">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2751">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2751">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2752">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2752">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2753">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2753">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2754">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2754">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2755">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2755">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2756">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2756">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2757">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2757">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2758">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2758">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2759">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2759">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2761">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2761">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="13900-2762">DXGI_FORMAT_R8G8 \_ uint<sup></sup> -Benutzerkonten (50)</span><span class="sxs-lookup"><span data-stu-id="13900-2762">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="13900-2763">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2763">Target</span></span> | <span data-ttu-id="13900-2764">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2764">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2765">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2765">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2766">16</span><span class="sxs-lookup"><span data-stu-id="13900-2766">16</span></span> |
| <span data-ttu-id="13900-2767">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2767">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2768">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2768">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2769">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2769">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2770">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2771">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2772">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2773">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2773">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2774">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2775">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2775">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2776">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2776">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2777">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2777">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2778">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2778">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2779">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2779">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2780">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2780">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2781">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2781">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2782">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2782">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2783">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2783">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2784">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2784">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2785">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2786">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2787">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2788">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2789">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2790">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2790">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2791">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2792">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2793">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2794">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2795">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2795">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2796">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2797">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2798">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2799">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2799">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2800">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2801">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2802">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2803">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2804">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2804">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2805">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2806">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2807">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2808">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2808">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2809">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2810">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2810">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2811">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="13900-2812">DXGI_FORMAT_R8G8 \_ snorm<sup></sup> -Kenn Wort (51)</span><span class="sxs-lookup"><span data-stu-id="13900-2812">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="13900-2813">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2813">Target</span></span> | <span data-ttu-id="13900-2814">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2815">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2816">16</span><span class="sxs-lookup"><span data-stu-id="13900-2816">16</span></span> |
| <span data-ttu-id="13900-2817">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2817">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2819">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2820">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2821">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2822">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2823">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2824">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2826">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2827">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2828">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2828">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2830">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2830">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2832">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2833">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2834">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2835">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2836">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2836">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2838">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2840">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2841">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2842">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2843">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2844">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2845">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2845">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2846">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2847">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2848">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2849">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2850">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2851">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2852">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2852">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2853">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2853">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2854">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2854">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-2856">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2857">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2858">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2859">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2860">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2860">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2861">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2862">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2862">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2863">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2864">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2864">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2865">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2865">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2866">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2866">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2867">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2867">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="13900-2868">DXGI_FORMAT_R8G8 \_ Sint<sup></sup> -SPT (52)</span><span class="sxs-lookup"><span data-stu-id="13900-2868">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="13900-2869">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2869">Target</span></span> | <span data-ttu-id="13900-2870">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2870">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2871">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2871">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2872">16</span><span class="sxs-lookup"><span data-stu-id="13900-2872">16</span></span> |
| <span data-ttu-id="13900-2873">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2873">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2874">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2874">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2875">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2876">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2877">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2878">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2879">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2880">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2881">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2882">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2883">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2884">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2885">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2886">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2886">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2887">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2888">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2888">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2889">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2890">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2891">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2892">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2893">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2894">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2895">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2896">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2896">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2897">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2898">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2899">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2900">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2902">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2903">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2904">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2905">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2905">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2906">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2906">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2907">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2907">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2908">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2908">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2909">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2909">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2910">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2910">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2911">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2911">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2912">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2912">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2913">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2914">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2915">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2916">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2917">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2917">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="13900-2918">DXGI_FORMAT_R16 \_ Typen losen<sup>PCs</sup> (53)</span><span class="sxs-lookup"><span data-stu-id="13900-2918">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="13900-2919">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2919">Target</span></span> | <span data-ttu-id="13900-2920">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2920">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2921">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2921">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2922">16</span><span class="sxs-lookup"><span data-stu-id="13900-2922">16</span></span> |
| <span data-ttu-id="13900-2923">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2923">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2924">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2924">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2925">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2925">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2926">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2926">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2927">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2927">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2928">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2928">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2929">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2929">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2930">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2930">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2931">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2931">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2932">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2932">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2933">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2934">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2935">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2936">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2936">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2937">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2938">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2938">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2939">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2939">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2940">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2940">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2941">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2941">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2942">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2942">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2943">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2943">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2944">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2944">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2945">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2945">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2946">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2946">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2947">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2947">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2948">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2948">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2949">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2949">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-2950">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-2950">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-2951">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-2951">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-2952">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-2952">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-2953">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-2953">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2954">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-2954">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-2955">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-2955">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-2956">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2956">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2957">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2957">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2958">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-2958">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-2959">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-2959">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-2960">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2960">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-2961">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-2961">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-2962">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-2962">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-2963">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-2963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-2964">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2964">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-2965">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-2965">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-2966">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2966">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-2967">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-2967">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="13900-2968">DXGI_FORMAT_R16 \_ float-"<sup>f</sup> " (54)</span><span class="sxs-lookup"><span data-stu-id="13900-2968">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="13900-2969">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2969">Target</span></span> | <span data-ttu-id="13900-2970">Support</span><span class="sxs-lookup"><span data-stu-id="13900-2970">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-2971">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-2971">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-2972">16</span><span class="sxs-lookup"><span data-stu-id="13900-2972">16</span></span> |
| <span data-ttu-id="13900-2973">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-2973">Format Support</span></span> | \- |
| <span data-ttu-id="13900-2974">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-2974">Buffer</span></span> | \- |
| <span data-ttu-id="13900-2975">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-2975">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-2976">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-2976">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-2977">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-2977">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-2978">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-2978">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-2979">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-2979">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-2980">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-2980">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-2981">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-2981">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-2982">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-2982">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-2983">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2983">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-2984">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2984">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-2985">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-2985">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-2986">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-2986">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-2987">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-2987">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-2988">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2988">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-2989">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-2989">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-2990">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2990">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2991">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-2991">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-2992">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-2992">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-2993">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-2993">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-2994">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2994">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2995">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-2995">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-2996">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-2996">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-2997">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-2997">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-2998">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-2998">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-2999">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-2999">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3000">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3000">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3001">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3001">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3002">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3002">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3003">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3003">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3004">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3004">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3005">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3005">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3006">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3007">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3008">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3009">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3010">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3010">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3011">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3012">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3013">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3014">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3015">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3016">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3016">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3017">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="13900-3018">DXGI_FORMAT_D16 \_ unorm<sup></sup> -Fehler (55)</span><span class="sxs-lookup"><span data-stu-id="13900-3018">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="13900-3019">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3019">Target</span></span> | <span data-ttu-id="13900-3020">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3020">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3021">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3022">16</span><span class="sxs-lookup"><span data-stu-id="13900-3022">16</span></span> |
| <span data-ttu-id="13900-3023">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3023">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3025">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3025">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3026">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3026">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3027">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3027">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3028">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3028">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3029">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3029">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3030">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3030">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3032">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3032">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3033">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3033">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3034">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3034">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3035">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3035">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3036">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3036">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3037">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3037">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3038">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3038">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3039">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3039">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3040">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3040">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3041">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3041">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3042">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3042">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3043">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3043">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3044">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3044">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3045">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3045">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3047">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3047">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3048">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3048">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3049">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3049">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3050">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3050">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3051">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3051">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3052">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3052">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3053">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3053">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3054">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3054">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3055">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3055">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3056">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3056">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3057">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3057">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3058">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3058">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3059">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3059">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-3061">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3061">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-3063">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3063">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-3065">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3066">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3066">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3067">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3068">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3069">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3070">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3071">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3072">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3072">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3073">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3073">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="13900-3074">DXGI_FORMAT_R16 \_ unorm<sup></sup> -Fehler (56)</span><span class="sxs-lookup"><span data-stu-id="13900-3074">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="13900-3075">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3075">Target</span></span> | <span data-ttu-id="13900-3076">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3076">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3077">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3077">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3078">16</span><span class="sxs-lookup"><span data-stu-id="13900-3078">16</span></span> |
| <span data-ttu-id="13900-3079">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3079">Format Support</span></span> | \- |
| <span data-ttu-id="13900-3080">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3080">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3081">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3081">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3082">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3082">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3083">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3083">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3084">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3084">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3085">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3086">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3086">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3087">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3087">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3088">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3088">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3089">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3089">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3090">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3090">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3091">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3091">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3092">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3092">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3093">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3093">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3094">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3094">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3095">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3096">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3097">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3098">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3099">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3100">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3101">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3102">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3102">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3103">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3104">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3105">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3106">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3107">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3108">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3109">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3110">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3111">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3111">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3112">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3112">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3113">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3113">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3114">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3114">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3115">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3115">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3116">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3116">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3117">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3117">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3118">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3118">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3119">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3120">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3121">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3122">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3122">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3123">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3123">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="13900-3124">DXGI_FORMAT_R16 \_ uint<sup></sup> -Benutzerkonten (57)</span><span class="sxs-lookup"><span data-stu-id="13900-3124">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="13900-3125">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3125">Target</span></span> | <span data-ttu-id="13900-3126">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3126">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3127">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3127">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3128">16</span><span class="sxs-lookup"><span data-stu-id="13900-3128">16</span></span> |
| <span data-ttu-id="13900-3129">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3129">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3131">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3131">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3132">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3132">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3133">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3133">Input Assembler Index Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3135">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3135">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3136">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3136">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3137">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3137">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3138">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3138">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3139">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3140">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3140">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3141">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3141">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3142">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3142">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3143">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3143">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3144">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3144">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3145">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3145">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3146">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3146">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3147">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3147">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3148">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3148">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3149">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3149">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3150">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3150">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3151">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3151">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3152">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3152">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3153">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3153">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3154">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3154">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3155">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3155">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3156">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3156">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3157">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3157">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3158">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3158">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3159">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3159">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3160">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3160">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3161">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3161">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3162">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3162">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3163">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3163">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3164">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3164">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3165">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3165">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3166">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3166">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3167">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3167">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3168">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3168">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3169">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3169">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3170">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3170">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3171">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3171">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3172">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3172">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3173">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3173">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3174">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3174">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3175">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="13900-3176">DXGI_FORMAT_R16 \_ snorm<sup></sup> -Kenn Wort (58)</span><span class="sxs-lookup"><span data-stu-id="13900-3176">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="13900-3177">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3177">Target</span></span> | <span data-ttu-id="13900-3178">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3178">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3179">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3180">16</span><span class="sxs-lookup"><span data-stu-id="13900-3180">16</span></span> |
| <span data-ttu-id="13900-3181">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3181">Format Support</span></span> | \- |
| <span data-ttu-id="13900-3182">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3182">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3183">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3183">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3184">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3185">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3185">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3186">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3186">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3187">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3188">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3188">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3189">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3190">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3190">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3191">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3191">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3192">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3192">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3193">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3193">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3194">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3194">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3195">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3195">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3196">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3196">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3197">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3198">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3199">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3200">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3201">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3202">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3203">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3204">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3204">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3205">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3206">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3207">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3208">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3209">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3210">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3211">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3212">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3213">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3213">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3214">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3214">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3215">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3215">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3216">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3216">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3217">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3217">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3218">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3218">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3219">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3219">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3220">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3220">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3221">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3221">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3222">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3222">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3223">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3223">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3224">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3224">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3225">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3225">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="13900-3226">DXGI_FORMAT_R16 \_ Sint<sup></sup> -SPT (59)</span><span class="sxs-lookup"><span data-stu-id="13900-3226">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="13900-3227">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3227">Target</span></span> | <span data-ttu-id="13900-3228">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3228">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3229">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3229">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3230">16</span><span class="sxs-lookup"><span data-stu-id="13900-3230">16</span></span> |
| <span data-ttu-id="13900-3231">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3231">Format Support</span></span> | \- |
| <span data-ttu-id="13900-3232">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3232">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3233">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3233">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3234">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3234">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3235">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3235">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3236">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3236">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3237">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3237">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3238">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3238">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3239">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3240">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3240">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3241">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3241">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3242">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3242">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3243">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3243">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3244">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3244">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3245">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3245">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3246">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3246">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3247">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3247">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3248">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3248">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3249">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3249">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3250">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3250">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3251">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3251">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3252">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3252">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3253">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3253">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3254">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3254">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3255">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3255">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3256">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3256">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3257">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3257">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3258">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3258">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3259">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3259">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3260">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3260">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3261">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3261">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3262">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3262">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3263">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3263">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3264">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3264">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3265">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3265">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3266">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3266">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3267">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3267">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3268">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3268">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3269">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3269">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3270">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3270">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3271">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3271">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3272">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3272">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3273">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3273">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3274">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3274">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3275">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3275">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="13900-3276">DXGI_FORMAT_R8 \_ Typen losen<sup>PCs</sup> (60)</span><span class="sxs-lookup"><span data-stu-id="13900-3276">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="13900-3277">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3277">Target</span></span> | <span data-ttu-id="13900-3278">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3278">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3279">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3279">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3280">8</span><span class="sxs-lookup"><span data-stu-id="13900-3280">8</span></span> |
| <span data-ttu-id="13900-3281">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3281">Format Support</span></span> | \- |
| <span data-ttu-id="13900-3282">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3282">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3283">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3283">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3284">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3284">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3285">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3285">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3286">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3286">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3287">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3287">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3288">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3288">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3289">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3289">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3290">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3290">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3291">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3292">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3293">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3294">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3294">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3295">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3296">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3296">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3297">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3297">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3298">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3298">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3299">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3299">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3300">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3300">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3301">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3301">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3302">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3302">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3303">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3303">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3304">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3304">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3305">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3305">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3306">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3306">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3307">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3307">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3308">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3308">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3309">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3309">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3310">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3310">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3311">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3311">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3312">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3312">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3313">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3313">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3314">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3314">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3315">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3315">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3316">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3316">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3317">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3317">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3318">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3318">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3319">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3319">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3320">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3320">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3321">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3321">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3322">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3322">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3323">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3323">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3324">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3324">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3325">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3325">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="13900-3326">DXGI_FORMAT_R8 \_ unorm<sup></sup> -Fehler (61)</span><span class="sxs-lookup"><span data-stu-id="13900-3326">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="13900-3327">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3327">Target</span></span> | <span data-ttu-id="13900-3328">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3328">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3329">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3329">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3330">8</span><span class="sxs-lookup"><span data-stu-id="13900-3330">8</span></span> |
| <span data-ttu-id="13900-3331">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3331">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3333">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3333">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3334">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3334">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3335">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3335">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3336">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3336">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3337">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3337">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3338">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3338">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3340">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3340">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3342">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3344">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3344">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3346">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3346">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3348">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3348">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3349">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3349">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3350">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3350">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3351">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3351">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3352">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3352">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3354">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3354">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3355">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3355">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3357">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3357">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3359">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3360">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3361">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3362">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3363">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3363">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3364">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3365">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3366">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3367">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3368">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3369">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3370">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3371">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3372">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3372">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3374">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3374">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3375">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3375">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3376">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3376">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3377">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3378">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3378">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3379">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3380">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3380">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3381">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3381">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3382">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3382">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3383">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3383">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3384">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3384">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3386">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3386">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="13900-3387">DXGI_FORMAT_R8 \_ uint<sup></sup> -Benutzerkonten (62)</span><span class="sxs-lookup"><span data-stu-id="13900-3387">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="13900-3388">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3388">Target</span></span> | <span data-ttu-id="13900-3389">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3389">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3390">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3390">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3391">8</span><span class="sxs-lookup"><span data-stu-id="13900-3391">8</span></span> |
| <span data-ttu-id="13900-3392">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3392">Format Support</span></span> | \- |
| <span data-ttu-id="13900-3393">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3393">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3394">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3394">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3395">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3395">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3396">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3396">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3397">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3397">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3398">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3399">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3399">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3400">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3400">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3401">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3401">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3402">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3402">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3403">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3403">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3404">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3404">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3405">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3405">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3406">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3406">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3407">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3407">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3408">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3408">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3409">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3410">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3411">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3412">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3413">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3414">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3415">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3415">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3416">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3416">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3417">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3417">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3418">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3418">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3419">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3419">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3420">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3420">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3421">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3421">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3422">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3422">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3423">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3423">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3424">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3424">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3425">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3426">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3427">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3428">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3429">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3429">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3430">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3431">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3431">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3432">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3433">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3434">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3435">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3435">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3436">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="13900-3437">DXGI_FORMAT_R8 \_ snorm<sup></sup> -Kenn Wort (63)</span><span class="sxs-lookup"><span data-stu-id="13900-3437">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="13900-3438">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3438">Target</span></span> | <span data-ttu-id="13900-3439">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3439">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3440">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3441">8</span><span class="sxs-lookup"><span data-stu-id="13900-3441">8</span></span> |
| <span data-ttu-id="13900-3442">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3442">Format Support</span></span> | \- |
| <span data-ttu-id="13900-3443">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3443">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3444">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3445">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3446">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3447">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3448">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3449">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3450">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3451">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3452">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3453">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3454">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3455">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3456">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3457">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3457">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3458">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3459">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3460">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3460">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3461">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3461">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3462">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3462">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3463">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3463">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3464">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3464">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3465">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3465">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3466">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3466">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3467">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3467">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3468">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3468">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3469">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3469">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3470">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3470">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3471">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3471">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3472">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3472">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3473">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3473">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3474">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3474">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3475">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3475">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3476">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3476">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3477">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3477">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3478">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3478">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3479">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3479">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3480">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3480">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3481">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3481">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3482">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3482">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3483">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3483">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3484">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3484">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3485">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3485">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3486">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3486">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="13900-3487">DXGI_FORMAT_R8 \_ Sint<sup></sup> -SPT (64)</span><span class="sxs-lookup"><span data-stu-id="13900-3487">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="13900-3488">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3488">Target</span></span> | <span data-ttu-id="13900-3489">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3489">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3490">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3490">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3491">8</span><span class="sxs-lookup"><span data-stu-id="13900-3491">8</span></span> |
| <span data-ttu-id="13900-3492">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3492">Format Support</span></span> | \- |
| <span data-ttu-id="13900-3493">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3493">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3494">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3495">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3496">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3497">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3498">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3499">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3499">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3500">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3501">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3501">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3502">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3502">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3503">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3503">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3504">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3504">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3505">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3505">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3506">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3506">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3507">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3507">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3508">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3508">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3509">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3509">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3510">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3510">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3511">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3511">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3512">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3512">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3513">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3513">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3514">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3514">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3515">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3515">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3516">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3516">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3517">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3517">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3518">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3518">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3519">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3519">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3520">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3520">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3521">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3521">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3522">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3522">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3523">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3523">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3524">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3524">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3525">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3525">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3526">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3526">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3527">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3527">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3528">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3528">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3529">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3529">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3530">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3530">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3531">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3531">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3532">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3532">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3533">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3533">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3534">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3534">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3535">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3535">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3536">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3536">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="13900-3537">DXGI_FORMAT_A8 \_ unorm<sup></sup> -Fehler (65)</span><span class="sxs-lookup"><span data-stu-id="13900-3537">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="13900-3538">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3538">Target</span></span> | <span data-ttu-id="13900-3539">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3539">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3540">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3540">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3541">8</span><span class="sxs-lookup"><span data-stu-id="13900-3541">8</span></span> |
| <span data-ttu-id="13900-3542">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3542">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3544">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3544">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3545">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3545">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3546">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3546">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3547">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3547">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3548">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3548">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3549">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3549">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3551">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3551">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3552">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3552">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3553">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3553">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3555">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3555">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3557">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3558">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3559">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3559">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3560">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3561">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3561">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3562">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3563">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3565">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3565">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3567">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3567">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3568">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3568">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3569">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3569">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3570">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3570">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3571">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3571">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3572">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3572">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3573">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3573">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3574">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3575">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3576">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3577">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3578">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3578">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3579">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3579">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3580">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3580">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3582">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3582">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3583">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3583">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3584">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3585">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3586">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3586">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3587">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3588">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3589">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3590">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3591">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3592">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3592">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3594">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="13900-3595">DXGI_FORMAT_R9G9B9E5 \_ sharede XP-<sup>LNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="13900-3595">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="13900-3596">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3596">Target</span></span> | <span data-ttu-id="13900-3597">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3597">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3598">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3599">32</span><span class="sxs-lookup"><span data-stu-id="13900-3599">32</span></span> |
| <span data-ttu-id="13900-3600">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3600">Format Support</span></span> | \- |
| <span data-ttu-id="13900-3601">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3601">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3602">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3602">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3603">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3603">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3604">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3604">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3605">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3605">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3606">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3607">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3607">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3608">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3608">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3609">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3609">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3610">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3610">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3611">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3612">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3613">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3613">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3614">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3615">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3615">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3616">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3617">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3618">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3618">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3619">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3619">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3620">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3620">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3621">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3621">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3622">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3622">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3623">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3623">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3624">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3624">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3625">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3625">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3626">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3626">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3627">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3627">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3628">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3628">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3629">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3629">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3630">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3630">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3631">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3631">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3632">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3632">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3633">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3633">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3634">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3634">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3635">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3635">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3636">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3636">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3637">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3637">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3638">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3638">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3639">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3639">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3640">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3640">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3641">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3641">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3642">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3642">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3643">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3643">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3644">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3644">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="13900-3645">DXGI_FORMAT_R8G8 \_ B8G8 \_ unorm<sup></sup> -Fehler (68)</span><span class="sxs-lookup"><span data-stu-id="13900-3645">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="13900-3646">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3646">Target</span></span> | <span data-ttu-id="13900-3647">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3647">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3648">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3648">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3649">16</span><span class="sxs-lookup"><span data-stu-id="13900-3649">16</span></span> |
| <span data-ttu-id="13900-3650">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3650">Format Support</span></span> | \- |
| <span data-ttu-id="13900-3651">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3651">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3652">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3652">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3653">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3653">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3654">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3654">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3655">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3655">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3656">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3657">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3658">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3659">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3659">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3660">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3660">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3661">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3661">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3662">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3662">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3663">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3663">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3664">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3664">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3665">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3665">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3666">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3666">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3667">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3667">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3668">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3668">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3669">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3669">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3670">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3670">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3671">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3671">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3672">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3672">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3673">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3673">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3674">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3674">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3675">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3675">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3676">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3676">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3677">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3677">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3678">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3678">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3679">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3679">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3680">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3680">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3681">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3681">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3682">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3682">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3683">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3684">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3685">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3686">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3687">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3687">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3688">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3688">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3689">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3689">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3690">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3690">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3691">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3691">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3692">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3692">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3693">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3693">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3694">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="13900-3695">DXGI_FORMAT_G8R8 \_ G8B8 \_ unorm<sup></sup> -Fehler (69)</span><span class="sxs-lookup"><span data-stu-id="13900-3695">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="13900-3696">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3696">Target</span></span> | <span data-ttu-id="13900-3697">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3697">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3698">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3699">16</span><span class="sxs-lookup"><span data-stu-id="13900-3699">16</span></span> |
| <span data-ttu-id="13900-3700">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3700">Format Support</span></span> | \- |
| <span data-ttu-id="13900-3701">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3701">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3702">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3702">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3703">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3703">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3704">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3704">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3705">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3705">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3706">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3706">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3707">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3707">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3708">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3708">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3709">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3709">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3710">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3711">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3712">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3713">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3713">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3714">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3715">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3715">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3716">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3716">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3717">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3717">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3718">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3719">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3720">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3721">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3722">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3723">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3723">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3724">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3725">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3726">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3727">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3728">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3729">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3730">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3730">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3731">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3731">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3732">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3732">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3733">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3733">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3734">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3734">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3735">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3735">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3736">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3736">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3737">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3737">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3738">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3738">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3739">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3739">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3740">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3741">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3741">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3742">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3742">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3743">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3743">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3744">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3744">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="13900-3745">DXGI_FORMAT_BC1 \_ typloses<sup>PCC</sup> (70)</span><span class="sxs-lookup"><span data-stu-id="13900-3745">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="13900-3746">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3746">Target</span></span> | <span data-ttu-id="13900-3747">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3747">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3748">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3748">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3749">4</span><span class="sxs-lookup"><span data-stu-id="13900-3749">4</span></span> |
| <span data-ttu-id="13900-3750">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3750">Format Support</span></span> | \- |
| <span data-ttu-id="13900-3751">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3751">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3752">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3752">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3753">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3753">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3754">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3754">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3755">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3755">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3756">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3756">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3757">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3758">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3758">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3759">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3759">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3760">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3760">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3761">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3761">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3762">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3762">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3763">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3763">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3764">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3764">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3765">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3765">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3766">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3766">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3767">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3767">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3768">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3768">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3769">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3769">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3770">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3770">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3771">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3771">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3772">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3772">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3773">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3773">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3774">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3774">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3775">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3775">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3776">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3776">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3777">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3777">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3778">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3778">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3779">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3779">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3780">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3780">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3781">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3781">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3782">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3782">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3783">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3783">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3784">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3784">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3785">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3785">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3786">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3786">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3787">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3787">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3788">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3788">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3789">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3789">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3790">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3790">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3791">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3791">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3792">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3792">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3793">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3793">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3794">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3794">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="13900-3795">DXGI_FORMAT_BC1 \_ unorm<sup></sup> -Fehler (71)</span><span class="sxs-lookup"><span data-stu-id="13900-3795">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="13900-3796">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3796">Target</span></span> | <span data-ttu-id="13900-3797">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3797">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3798">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3798">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3799">4</span><span class="sxs-lookup"><span data-stu-id="13900-3799">4</span></span> |
| <span data-ttu-id="13900-3800">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3800">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3802">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3802">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3803">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3803">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3804">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3805">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3806">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3807">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3810">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3812">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3812">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3814">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3814">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3816">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3816">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3817">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3817">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3818">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3818">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3819">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3819">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3820">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3820">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3822">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3822">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3823">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3823">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3824">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3824">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3825">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3825">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3826">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3826">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3827">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3827">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3828">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3828">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3829">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3829">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3830">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3830">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3831">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3831">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3832">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3832">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3833">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3833">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3834">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3834">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3835">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3835">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3836">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3836">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3837">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3837">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3838">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3838">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3840">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3841">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3842">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3843">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3844">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3845">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3846">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3847">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3848">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3849">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3850">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3850">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3852">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3852">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="13900-3853">DXGI_FORMAT_BC1 \_ unorm \_ sRGB<sup></sup> -Fehler (72)</span><span class="sxs-lookup"><span data-stu-id="13900-3853">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="13900-3854">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3854">Target</span></span> | <span data-ttu-id="13900-3855">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3855">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3856">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3856">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3857">4</span><span class="sxs-lookup"><span data-stu-id="13900-3857">4</span></span> |
| <span data-ttu-id="13900-3858">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3858">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3860">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3860">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3861">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3861">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3862">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3862">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3863">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3863">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3864">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3864">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3865">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3865">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3867">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3867">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3868">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3870">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3870">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3872">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3872">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3874">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3874">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3875">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3875">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3876">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3876">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3877">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3877">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3878">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3878">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3880">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3881">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3882">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3883">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3884">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3885">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3886">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3887">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3887">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3888">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3889">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3890">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3891">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3892">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3893">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3894">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3895">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3896">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3896">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3898">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3898">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3899">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3899">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3900">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3900">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3901">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3901">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3902">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3902">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3903">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3903">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3904">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3904">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3905">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3906">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3907">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3908">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3908">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3910">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3910">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="13900-3911">DXGI_FORMAT_BC2 \_ typloses<sup>PCC</sup> (73)</span><span class="sxs-lookup"><span data-stu-id="13900-3911">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="13900-3912">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3912">Target</span></span> | <span data-ttu-id="13900-3913">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3913">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3914">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3914">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3915">8</span><span class="sxs-lookup"><span data-stu-id="13900-3915">8</span></span> |
| <span data-ttu-id="13900-3916">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3916">Format Support</span></span> | \- |
| <span data-ttu-id="13900-3917">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3917">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3918">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3918">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3919">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3919">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3920">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3920">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3921">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3921">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3922">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3922">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-3923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3923">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3924">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-3925">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3925">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-3926">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3926">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-3927">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3927">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3928">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3928">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3929">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3929">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3930">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3930">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3931">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3931">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-3932">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3932">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3933">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3933">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3934">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3934">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3935">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3935">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3936">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3936">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3937">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3937">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3938">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3938">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3939">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3939">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3940">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3940">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3941">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3941">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3942">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3942">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3943">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3943">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-3944">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-3944">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-3945">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-3945">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-3946">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-3946">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3947">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-3947">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-3948">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-3948">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-3949">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3949">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3950">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3950">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3951">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-3951">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-3952">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-3952">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-3953">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3953">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-3954">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-3954">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-3955">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-3955">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-3956">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-3956">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-3957">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3957">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-3958">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-3958">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-3959">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3959">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-3960">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-3960">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="13900-3961">DXGI_FORMAT_BC2 \_ unorm<sup></sup> -Fehler (74)</span><span class="sxs-lookup"><span data-stu-id="13900-3961">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="13900-3962">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3962">Target</span></span> | <span data-ttu-id="13900-3963">Support</span><span class="sxs-lookup"><span data-stu-id="13900-3963">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-3964">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-3964">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-3965">8</span><span class="sxs-lookup"><span data-stu-id="13900-3965">8</span></span> |
| <span data-ttu-id="13900-3966">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-3966">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3968">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-3968">Buffer</span></span> | \- |
| <span data-ttu-id="13900-3969">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-3969">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-3970">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-3970">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-3971">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-3971">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-3972">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-3972">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-3973">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-3973">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3975">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-3975">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-3976">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-3976">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3978">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-3978">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3980">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3980">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3982">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3982">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-3983">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-3983">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-3984">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-3984">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-3985">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-3985">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-3986">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3986">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-3988">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-3988">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-3989">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3989">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3990">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-3990">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-3991">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-3991">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-3992">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-3992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-3993">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3994">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-3994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-3995">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-3995">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-3996">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-3996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-3997">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-3997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-3998">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-3998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-3999">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-3999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4000">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4000">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4001">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4002">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4003">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4004">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4004">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4006">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4007">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4008">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4009">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4010">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4010">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4011">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4012">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4013">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4014">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4015">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4016">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4016">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4018">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4018">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="13900-4019">DXGI_FORMAT_BC2 \_ unorm \_ sRGB<sup></sup> -Fehler (75)</span><span class="sxs-lookup"><span data-stu-id="13900-4019">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="13900-4020">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4020">Target</span></span> | <span data-ttu-id="13900-4021">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4021">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4022">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4022">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4023">8</span><span class="sxs-lookup"><span data-stu-id="13900-4023">8</span></span> |
| <span data-ttu-id="13900-4024">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4024">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4026">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4026">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4027">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4027">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4028">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4029">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4029">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4030">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4030">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4031">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4031">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4033">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4033">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4034">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4034">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4036">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4036">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4038">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4038">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4040">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4040">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4041">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4041">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4042">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4042">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4043">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4043">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4044">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4044">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4046">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4046">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4047">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4047">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4048">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4048">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4049">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4049">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4050">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4050">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4051">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4051">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4052">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4052">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4053">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4053">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4054">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4054">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4055">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4055">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4056">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4057">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4058">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4059">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4060">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4060">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4061">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4061">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4062">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4062">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4064">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4064">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4065">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4065">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4066">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4066">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4067">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4067">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4068">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4068">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4069">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4069">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4070">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4070">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4071">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4072">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4072">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4073">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4073">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4074">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4074">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4076">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="13900-4077">DXGI_FORMAT_BC3 \_ typloses<sup>PCC</sup> (76)</span><span class="sxs-lookup"><span data-stu-id="13900-4077">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="13900-4078">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4078">Target</span></span> | <span data-ttu-id="13900-4079">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4079">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4080">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4081">8</span><span class="sxs-lookup"><span data-stu-id="13900-4081">8</span></span> |
| <span data-ttu-id="13900-4082">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4082">Format Support</span></span> | \- |
| <span data-ttu-id="13900-4083">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4083">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4084">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4085">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4086">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4087">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4088">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-4089">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4089">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4090">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4090">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-4091">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4091">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-4092">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4092">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-4093">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4093">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4094">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4094">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4095">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4095">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4096">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4096">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4097">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4097">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-4098">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4098">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4099">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4099">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4100">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4101">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4102">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4103">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4104">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4105">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4105">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4106">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4107">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4108">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4109">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4110">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4111">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4112">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4112">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4113">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4113">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4114">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4114">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-4115">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4116">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4117">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4118">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4119">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4119">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4120">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4121">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4122">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4122">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4123">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4123">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4124">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4124">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4125">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4125">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-4126">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4126">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="13900-4127">DXGI_FORMAT_BC3 \_ unorm<sup></sup> -Fehler (77)</span><span class="sxs-lookup"><span data-stu-id="13900-4127">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="13900-4128">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4128">Target</span></span> | <span data-ttu-id="13900-4129">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4129">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4130">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4131">8</span><span class="sxs-lookup"><span data-stu-id="13900-4131">8</span></span> |
| <span data-ttu-id="13900-4132">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4132">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4134">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4134">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4135">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4135">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4136">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4136">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4137">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4137">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4138">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4139">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4139">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4141">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4142">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4142">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4144">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4144">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4146">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4146">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4148">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4148">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4149">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4149">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4150">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4150">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4151">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4151">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4152">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4152">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4154">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4154">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4155">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4155">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4156">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4156">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4157">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4157">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4158">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4158">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4159">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4159">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4160">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4160">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4161">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4161">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4162">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4162">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4163">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4163">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4164">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4164">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4165">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4165">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4166">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4166">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4167">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4167">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4168">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4168">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4169">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4169">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4170">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4170">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4172">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4172">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4173">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4173">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4174">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4174">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4175">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4175">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4176">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4176">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4177">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4177">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4178">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4178">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4179">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4179">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4180">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4180">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4181">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4181">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4182">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4182">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4184">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4184">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="13900-4185">DXGI_FORMAT_BC3 \_ unorm \_ sRGB<sup></sup> -Fehler (78)</span><span class="sxs-lookup"><span data-stu-id="13900-4185">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="13900-4186">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4186">Target</span></span> | <span data-ttu-id="13900-4187">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4187">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4188">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4188">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4189">8</span><span class="sxs-lookup"><span data-stu-id="13900-4189">8</span></span> |
| <span data-ttu-id="13900-4190">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4190">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4192">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4192">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4193">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4193">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4194">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4194">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4195">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4195">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4196">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4196">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4197">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4197">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4199">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4199">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4200">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4202">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4202">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4204">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4204">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4206">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4207">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4208">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4209">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4210">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4210">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4212">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4213">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4214">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4215">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4216">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4217">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4218">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4219">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4219">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4220">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4221">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4222">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4223">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4224">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4225">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4226">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4227">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4228">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4228">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4230">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4230">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4231">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4231">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4232">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4232">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4233">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4233">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4234">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4234">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4235">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4235">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4236">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4236">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4237">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4237">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4238">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4238">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4239">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4239">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4240">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4240">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4242">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4242">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="13900-4243">DXGI_FORMAT_BC4 \_ typloses<sup>PCC</sup> (79)</span><span class="sxs-lookup"><span data-stu-id="13900-4243">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="13900-4244">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4244">Target</span></span> | <span data-ttu-id="13900-4245">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4245">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4246">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4246">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4247">4</span><span class="sxs-lookup"><span data-stu-id="13900-4247">4</span></span> |
| <span data-ttu-id="13900-4248">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4248">Format Support</span></span> | \- |
| <span data-ttu-id="13900-4249">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4249">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4250">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4250">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4251">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4251">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4252">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4252">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4253">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4253">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4254">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-4255">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4255">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4256">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4256">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-4257">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4257">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-4258">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4258">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-4259">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4260">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4261">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4261">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4262">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4263">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4263">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-4264">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4264">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4265">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4265">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4266">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4266">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4267">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4267">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4268">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4268">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4269">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4269">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4270">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4270">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4271">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4271">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4272">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4272">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4273">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4273">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4274">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4274">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4275">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4275">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4276">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4276">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4277">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4277">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4278">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4278">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4279">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4279">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4280">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4280">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-4281">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4281">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4282">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4282">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4283">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4283">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4284">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4284">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4285">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4285">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4286">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4286">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4287">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4287">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4288">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4289">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4290">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4291">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4291">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-4292">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="13900-4293">DXGI_FORMAT_BC4 \_ unorm<sup></sup> -Fehler (80)</span><span class="sxs-lookup"><span data-stu-id="13900-4293">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="13900-4294">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4294">Target</span></span> | <span data-ttu-id="13900-4295">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4295">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4296">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4297">4</span><span class="sxs-lookup"><span data-stu-id="13900-4297">4</span></span> |
| <span data-ttu-id="13900-4298">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4298">Format Support</span></span> | \- |
| <span data-ttu-id="13900-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4299">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4300">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4301">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4302">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4304">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-4305">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4305">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4306">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4306">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-4307">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4307">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-4308">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4308">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-4309">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4309">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4310">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4310">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4311">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4311">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4312">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4312">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4313">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4313">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-4314">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4314">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4315">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4315">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4316">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4316">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4317">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4317">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4318">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4318">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4319">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4319">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4320">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4320">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4321">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4321">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4322">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4322">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4323">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4323">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4324">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4324">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4325">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4325">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4326">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4326">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4327">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4327">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4328">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4328">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4329">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4329">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4330">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4330">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-4331">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4332">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4333">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4334">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4335">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4335">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4336">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4337">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4337">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4338">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4338">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4339">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4339">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4340">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4340">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4341">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4341">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-4342">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4342">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="13900-4343">DXGI_FORMAT_BC4 \_ snorm<sup></sup> -snorm (81)</span><span class="sxs-lookup"><span data-stu-id="13900-4343">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="13900-4344">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4344">Target</span></span> | <span data-ttu-id="13900-4345">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4345">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4346">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4346">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4347">4</span><span class="sxs-lookup"><span data-stu-id="13900-4347">4</span></span> |
| <span data-ttu-id="13900-4348">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4348">Format Support</span></span> | \- |
| <span data-ttu-id="13900-4349">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4349">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4350">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4350">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4351">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4352">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4353">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4354">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4354">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-4355">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4355">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4356">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4356">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-4357">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4357">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-4358">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4358">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-4359">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4359">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4360">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4360">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4361">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4361">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4362">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4362">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4363">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4363">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-4364">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4364">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4365">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4365">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4366">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4366">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4367">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4367">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4368">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4368">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4369">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4369">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4370">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4370">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4371">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4371">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4372">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4372">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4373">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4373">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4374">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4374">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4375">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4375">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4376">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4376">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4377">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4377">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4378">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4378">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4379">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4379">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4380">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4380">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-4381">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4381">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4382">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4382">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4383">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4383">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4384">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4384">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4385">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4385">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4386">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4386">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4387">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4387">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4388">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4388">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4389">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4389">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4390">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4390">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4391">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4391">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-4392">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4392">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="13900-4393">DXGI_FORMAT_BC5 \_ typloses<sup>PCC</sup> (82)</span><span class="sxs-lookup"><span data-stu-id="13900-4393">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="13900-4394">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4394">Target</span></span> | <span data-ttu-id="13900-4395">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4395">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4396">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4396">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4397">8</span><span class="sxs-lookup"><span data-stu-id="13900-4397">8</span></span> |
| <span data-ttu-id="13900-4398">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4398">Format Support</span></span> | \- |
| <span data-ttu-id="13900-4399">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4399">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4400">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4400">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4401">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4402">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4403">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4404">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-4405">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4405">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4406">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4406">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-4407">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4407">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-4408">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4408">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-4409">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4409">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4410">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4410">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4411">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4411">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4412">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4412">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4413">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4413">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-4414">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4414">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4415">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4415">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4416">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4417">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4418">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4419">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4420">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4421">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4421">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4422">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4422">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4423">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4423">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4424">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4424">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4425">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4425">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4426">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4426">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4427">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4427">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4428">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4428">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4429">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4429">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4430">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4430">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-4431">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4431">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4432">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4432">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4433">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4433">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4434">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4434">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4435">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4435">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4436">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4437">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4438">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4439">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4440">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4441">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4441">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-4442">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="13900-4443">DXGI_FORMAT_BC5 \_ unorm<sup></sup> -Fehler (83)</span><span class="sxs-lookup"><span data-stu-id="13900-4443">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="13900-4444">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4444">Target</span></span> | <span data-ttu-id="13900-4445">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4445">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4446">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4447">8</span><span class="sxs-lookup"><span data-stu-id="13900-4447">8</span></span> |
| <span data-ttu-id="13900-4448">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4448">Format Support</span></span> | \- |
| <span data-ttu-id="13900-4449">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4449">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4450">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4451">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4452">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4453">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4454">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4454">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-4455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4455">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4456">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4456">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-4457">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4457">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-4458">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4458">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-4459">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4459">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4460">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4460">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4461">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4461">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4462">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4462">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4463">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4463">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-4464">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4464">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4465">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4465">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4466">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4466">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4467">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4467">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4468">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4468">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4469">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4470">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4471">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4471">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4472">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4473">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4474">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4475">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4476">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4476">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4477">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4478">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4479">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4480">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4480">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-4481">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4481">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4482">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4482">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4483">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4483">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4484">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4484">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4485">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4485">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4486">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4486">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4487">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4487">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4488">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4488">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4489">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4489">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4490">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4490">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4491">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4491">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-4492">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4492">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="13900-4493">DXGI_FORMAT_BC5 \_ snorm<sup></sup> -snorm (84)</span><span class="sxs-lookup"><span data-stu-id="13900-4493">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="13900-4494">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4494">Target</span></span> | <span data-ttu-id="13900-4495">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4495">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4496">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4496">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4497">8</span><span class="sxs-lookup"><span data-stu-id="13900-4497">8</span></span> |
| <span data-ttu-id="13900-4498">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4498">Format Support</span></span> | \- |
| <span data-ttu-id="13900-4499">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4499">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4500">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4500">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4501">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4501">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4502">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4502">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4503">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4503">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4504">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4504">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-4505">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4505">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4506">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-4507">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4507">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-4508">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4508">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-4509">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4509">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4510">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4510">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4511">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4511">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4512">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4512">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4513">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4513">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-4514">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4515">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4516">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4517">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4518">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4519">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4520">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4521">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4521">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4522">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4523">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4524">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4525">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4526">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4526">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4527">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4528">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4529">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4530">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4530">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-4531">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4531">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4532">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4532">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4533">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4533">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4534">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4534">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4535">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4535">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4536">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4536">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4537">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4537">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4538">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4538">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4539">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4539">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4540">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4540">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4541">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4541">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-4542">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="13900-4543">DXGI_FORMAT_B5G6R5 \_ unorm<sup></sup> -Fehler (85)</span><span class="sxs-lookup"><span data-stu-id="13900-4543">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="13900-4544">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4544">Target</span></span> | <span data-ttu-id="13900-4545">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4546">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4547">16</span><span class="sxs-lookup"><span data-stu-id="13900-4547">16</span></span> |
| <span data-ttu-id="13900-4548">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4548">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4550">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4551">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4552">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4553">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4554">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4555">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4555">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4557">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4558">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4560">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4560">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4562">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4562">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4564">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4564">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4565">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4565">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4566">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4566">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4567">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4567">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4568">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4568">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4570">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4570">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4572">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4574">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4574">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4576">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4577">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4578">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4579">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4580">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4580">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4581">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4582">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4583">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4584">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4585">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4585">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4586">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4587">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4588">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4589">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4589">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4591">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4591">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4593">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4593">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4595">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4595">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4597">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4597">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4599">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4599">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4600">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4600">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4601">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4601">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4602">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4602">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4603">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4603">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4604">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4604">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4605">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4605">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-4606">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4606">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="13900-4607">DXGI_FORMAT_B5G5R5A1 \_ unorm<sup></sup> -Fehler (86)</span><span class="sxs-lookup"><span data-stu-id="13900-4607">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="13900-4608">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4608">Target</span></span> | <span data-ttu-id="13900-4609">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4609">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4610">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4610">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4611">16</span><span class="sxs-lookup"><span data-stu-id="13900-4611">16</span></span> |
| <span data-ttu-id="13900-4612">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4612">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4614">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4614">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4615">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4615">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4616">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4616">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4617">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4617">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4618">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4618">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4619">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4621">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4622">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4622">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4624">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4624">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4626">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4626">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4628">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4628">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4629">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4629">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4630">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4630">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4631">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4631">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4632">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4632">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4634">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4634">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4635">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4635">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4636">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4636">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4637">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4637">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4638">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4638">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4639">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4639">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4640">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4640">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4641">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4641">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4642">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4642">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4643">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4643">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4644">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4644">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4645">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4645">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4646">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4646">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4647">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4647">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4648">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4648">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4649">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4649">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4650">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4650">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4652">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4652">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4653">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4653">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4654">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4654">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4655">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4655">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4656">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4656">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4657">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4658">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4658">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4659">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4659">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4660">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4660">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4661">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4661">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4662">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4662">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-4663">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="13900-4664">DXGI_FORMAT_B8G8R8A8 \_ Typen losen<sup>PCs</sup> (90)</span><span class="sxs-lookup"><span data-stu-id="13900-4664">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="13900-4665">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4665">Target</span></span> | <span data-ttu-id="13900-4666">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4666">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4667">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4668">32</span><span class="sxs-lookup"><span data-stu-id="13900-4668">32</span></span> |
| <span data-ttu-id="13900-4669">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4669">Format Support</span></span> | \- |
| <span data-ttu-id="13900-4670">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4670">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4671">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4672">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4673">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4674">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4675">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4675">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4676">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4677">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4677">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-4678">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4678">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-4679">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4679">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-4680">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4681">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4682">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4682">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4683">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4684">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4684">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-4685">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4685">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4686">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4686">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4687">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4687">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4688">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4688">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4689">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4689">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4690">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4690">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4691">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4691">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4692">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4692">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4693">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4693">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4694">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4694">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4695">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4695">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4696">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4696">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4697">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4697">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4698">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4698">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4699">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4699">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4700">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4700">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4701">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4701">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-4702">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4702">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4703">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4703">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4704">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4704">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4705">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4705">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4706">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4707">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4708">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4709">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4710">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4711">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4712">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-4713">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="13900-4714">DXGI_FORMAT_B8G8R8A8 \_ unorm<sup></sup> -Fehler (87)</span><span class="sxs-lookup"><span data-stu-id="13900-4714">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="13900-4715">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4715">Target</span></span> | <span data-ttu-id="13900-4716">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4717">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4718">32</span><span class="sxs-lookup"><span data-stu-id="13900-4718">32</span></span> |
| <span data-ttu-id="13900-4719">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4719">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4721">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4722">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4723">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4724">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4726">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4728">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4730">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4732">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4732">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4734">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4734">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4736">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4737">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4738">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4738">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4739">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4740">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4740">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4742">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4742">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4744">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4746">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4746">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4748">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4749">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4750">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4751">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4752">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4752">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4753">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4754">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4755">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4756">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4757">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4757">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4758">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4759">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4760">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4761">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4761">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4763">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4763">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4765">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4765">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4767">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4767">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4769">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4769">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4771">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4771">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4772">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4772">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4774">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4774">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4775">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4775">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4776">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4776">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4778">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4778">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4780">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4780">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4782">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="13900-4783">DXGI_FORMAT_B8G8R8A8 \_ unorm \_ sRGB<sup></sup> -Fehler (91)</span><span class="sxs-lookup"><span data-stu-id="13900-4783">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="13900-4784">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4784">Target</span></span> | <span data-ttu-id="13900-4785">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4785">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4786">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4787">32</span><span class="sxs-lookup"><span data-stu-id="13900-4787">32</span></span> |
| <span data-ttu-id="13900-4788">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4788">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4790">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4790">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4791">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4791">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4792">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4792">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4793">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4793">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4794">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4794">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4795">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4797">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4799">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4799">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4801">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4801">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4803">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4803">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4805">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4805">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4806">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4806">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4807">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4807">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4808">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4808">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4809">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4809">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4811">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4811">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4813">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4815">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4815">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4817">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4817">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4818">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4818">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4819">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4819">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4820">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4820">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4821">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4821">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4822">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4822">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4823">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4823">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4824">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4824">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4825">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4825">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4826">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4826">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4827">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4827">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4828">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4828">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4829">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4829">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4830">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4830">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4832">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4832">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4834">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4834">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4836">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4836">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4838">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4838">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4840">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4840">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4841">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4841">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4843">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4843">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4844">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4844">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4845">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4845">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4847">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4847">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4849">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4849">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4851">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="13900-4852">DXGI_FORMAT_B8G8R8X8 \_ Typen losen<sup>PCs</sup> (92)</span><span class="sxs-lookup"><span data-stu-id="13900-4852">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="13900-4853">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4853">Target</span></span> | <span data-ttu-id="13900-4854">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4854">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4855">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4856">32</span><span class="sxs-lookup"><span data-stu-id="13900-4856">32</span></span> |
| <span data-ttu-id="13900-4857">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4857">Format Support</span></span> | \- |
| <span data-ttu-id="13900-4858">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4858">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4859">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4860">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4861">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4862">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4863">Texture2D</span></span> | \- |
| <span data-ttu-id="13900-4864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4864">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-4865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4865">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-4866">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-4867">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-4868">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4869">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4870">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4870">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4871">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4872">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4872">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-4873">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-4874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4874">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4875">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4876">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4877">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4878">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4879">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4880">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4880">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4881">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4882">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4883">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4884">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4886">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4887">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4888">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4889">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-4890">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4891">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-4892">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-4893">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-4894">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4894">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4895">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4896">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4897">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4898">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-4899">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-4900">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4900">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-4901">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="13900-4902">DXGI_FORMAT_B8G8R8X8 \_ unorm<sup></sup> -Fehler (88)</span><span class="sxs-lookup"><span data-stu-id="13900-4902">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="13900-4903">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4903">Target</span></span> | <span data-ttu-id="13900-4904">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4904">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4905">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4906">32</span><span class="sxs-lookup"><span data-stu-id="13900-4906">32</span></span> |
| <span data-ttu-id="13900-4907">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4907">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4909">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4909">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4910">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4911">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4912">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4913">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4914">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4916">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4918">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4918">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4920">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4920">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4922">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4922">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4924">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4924">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4925">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4925">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4926">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4926">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4927">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4927">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4928">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4928">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4930">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4930">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4932">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4932">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4934">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4934">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4936">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-4936">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-4937">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4937">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-4938">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4938">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4939">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-4939">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-4940">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-4940">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-4941">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-4941">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-4942">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4942">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-4943">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-4943">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-4944">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-4944">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-4945">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-4945">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-4946">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-4946">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-4947">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-4947">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4948">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-4948">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-4949">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-4949">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4951">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4951">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4953">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-4953">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4955">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-4955">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4957">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-4957">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4959">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-4959">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-4960">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-4960">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-4961">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-4961">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-4962">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-4962">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-4963">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4963">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4965">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-4965">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-4967">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4967">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4969">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-4969">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="13900-4970">DXGI_FORMAT_B8G8R8X8 \_ unorm \_ sRGB<sup></sup> -Fehler (93)</span><span class="sxs-lookup"><span data-stu-id="13900-4970">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="13900-4971">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-4971">Target</span></span> | <span data-ttu-id="13900-4972">Support</span><span class="sxs-lookup"><span data-stu-id="13900-4972">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-4973">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-4973">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-4974">32</span><span class="sxs-lookup"><span data-stu-id="13900-4974">32</span></span> |
| <span data-ttu-id="13900-4975">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-4975">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4977">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-4977">Buffer</span></span> | \- |
| <span data-ttu-id="13900-4978">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-4978">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-4979">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-4979">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-4980">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-4980">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-4981">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-4981">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-4982">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-4982">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4984">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-4984">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4986">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-4986">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4988">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-4988">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4990">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4990">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4992">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4992">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-4993">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-4993">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-4994">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-4994">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-4995">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-4995">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-4996">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4996">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-4998">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-4998">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5000">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5000">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5002">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5002">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5004">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5004">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5005">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5005">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5006">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5006">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5007">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5007">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5008">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5008">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5009">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5009">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5010">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5010">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5011">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5011">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5012">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5012">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5013">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5013">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5014">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5014">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5015">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5015">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5016">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5016">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5017">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5017">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5019">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5019">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5021">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5021">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5023">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5023">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5025">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5025">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5027">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5027">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5028">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5028">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5029">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5029">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5030">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5030">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-5031">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5031">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-5032">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5032">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-5033">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5033">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5035">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5035">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="13900-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="13900-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="13900-5037">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5037">Target</span></span> | <span data-ttu-id="13900-5038">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5038">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5039">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5039">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5040">32</span><span class="sxs-lookup"><span data-stu-id="13900-5040">32</span></span> |
| <span data-ttu-id="13900-5041">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5041">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5043">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5043">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5044">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5044">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5045">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5045">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5046">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5046">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5047">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5047">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5048">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5050">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5051">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5052">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5053">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5054">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5055">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5056">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5056">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5057">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5058">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5058">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5059">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5060">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5061">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5062">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5063">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5064">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5065">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5066">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5066">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5067">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5068">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5069">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5070">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5071">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5072">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5073">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5074">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5075">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5075">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5077">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5078">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5079">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5080">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5081">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5081">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5082">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5083">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5084">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5084">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5086">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5086">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5088">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5088">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5090">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5090">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5091">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="13900-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="13900-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="13900-5093">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5093">Target</span></span> | <span data-ttu-id="13900-5094">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5094">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5095">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5096">32</span><span class="sxs-lookup"><span data-stu-id="13900-5096">32</span></span> |
| <span data-ttu-id="13900-5097">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5097">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5099">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5099">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5100">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5101">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5102">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5103">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5104">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5106">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5107">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5107">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5108">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5108">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5109">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5109">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5110">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5110">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5111">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5111">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5112">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5112">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5113">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5113">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5114">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5114">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5115">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5115">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5116">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5116">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5117">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5117">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5118">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5118">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5119">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5119">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5120">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5120">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5121">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5121">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5122">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5122">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5123">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5123">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5124">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5124">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5125">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5125">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5126">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5126">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5127">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5127">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5128">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5128">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5129">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5129">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5130">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5130">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5131">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5131">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5133">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5133">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5134">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5134">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5135">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5135">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5136">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5136">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5137">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5137">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5138">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5138">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5139">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5139">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5140">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5140">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5142">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5142">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5144">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5144">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5146">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5146">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5147">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="13900-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="13900-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="13900-5149">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5149">Target</span></span> | <span data-ttu-id="13900-5150">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5150">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5151">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5152">64</span><span class="sxs-lookup"><span data-stu-id="13900-5152">64</span></span> |
| <span data-ttu-id="13900-5153">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5153">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5155">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5155">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5156">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5157">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5158">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5159">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5160">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5162">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5163">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5164">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5164">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5165">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5165">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5166">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5166">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5167">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5167">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5168">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5168">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5169">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5169">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5170">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5170">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5171">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5171">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5172">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5172">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5173">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5173">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5174">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5174">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5175">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5175">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5176">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5176">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5177">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5177">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5178">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5178">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5179">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5179">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5180">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5180">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5181">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5181">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5182">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5182">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5183">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5183">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5184">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5184">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5185">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5185">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5186">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5186">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5187">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5187">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5189">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5189">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5190">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5190">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5191">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5191">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5192">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5192">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5193">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5193">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5194">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5194">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5195">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5195">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5196">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5196">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5198">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5198">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5200">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5200">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5202">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5202">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5203">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5203">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="13900-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="13900-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="13900-5205">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5205">Target</span></span> | <span data-ttu-id="13900-5206">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5206">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5207">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5207">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5208">8</span><span class="sxs-lookup"><span data-stu-id="13900-5208">8</span></span> |
| <span data-ttu-id="13900-5209">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5209">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5211">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5211">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5212">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5212">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5213">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5213">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5214">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5214">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5215">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5215">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5216">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5218">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5219">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5220">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5220">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5221">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5221">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5222">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5222">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5223">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5223">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5224">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5224">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5225">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5226">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5226">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5227">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5227">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5228">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5228">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5229">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5229">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5230">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5230">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5231">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5231">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5232">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5232">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5233">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5233">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5234">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5234">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5235">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5235">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5236">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5237">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5238">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5239">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5240">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5241">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5241">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5242">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5242">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5243">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5243">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5245">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5246">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5247">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5248">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5249">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5249">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5250">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5251">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5252">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5252">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5254">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5254">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5256">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5256">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5258">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5258">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5259">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5259">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="13900-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="13900-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="13900-5261">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5261">Target</span></span> | <span data-ttu-id="13900-5262">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5262">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5263">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5263">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5264">16</span><span class="sxs-lookup"><span data-stu-id="13900-5264">16</span></span> |
| <span data-ttu-id="13900-5265">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5265">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5267">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5267">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5268">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5268">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5269">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5269">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5270">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5270">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5271">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5271">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5272">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5272">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5274">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5274">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5275">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5275">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5276">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5276">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5277">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5277">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5278">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5278">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5279">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5279">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5280">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5280">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5281">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5281">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5282">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5282">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5283">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5283">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5284">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5284">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5285">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5286">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5286">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5287">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5287">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5288">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5288">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5289">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5289">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5290">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5290">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5291">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5291">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5292">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5292">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5293">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5293">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5294">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5294">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5295">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5295">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5296">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5296">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5297">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5297">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5298">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5298">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5299">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5299">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5301">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5301">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5302">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5302">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5303">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5303">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5304">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5304">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5305">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5305">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5306">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5306">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5307">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5307">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5308">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5308">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5310">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5310">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5312">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5312">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5314">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5314">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5315">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5315">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="13900-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="13900-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="13900-5317">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5317">Target</span></span> | <span data-ttu-id="13900-5318">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5318">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5319">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5320">16</span><span class="sxs-lookup"><span data-stu-id="13900-5320">16</span></span> |
| <span data-ttu-id="13900-5321">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5321">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5323">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5323">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5324">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5324">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5325">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5325">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5326">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5326">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5327">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5328">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5330">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5331">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5331">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5332">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5332">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5333">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5334">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5334">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5335">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5335">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5336">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5336">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5337">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5337">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5338">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5338">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5339">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5341">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5342">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5343">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5344">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5345">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5346">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5347">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5348">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5349">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5350">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5351">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5352">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5353">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5354">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5355">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5355">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5357">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5358">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5359">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5360">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5361">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5362">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5363">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5364">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5364">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5366">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5366">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5368">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5368">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5370">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5370">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5371">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5371">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="13900-5372">DXGI_FORMAT_420 nicht transparent \_ <sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="13900-5372">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="13900-5373">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5373">Target</span></span> | <span data-ttu-id="13900-5374">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5374">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5375">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5375">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5376">8</span><span class="sxs-lookup"><span data-stu-id="13900-5376">8</span></span> |
| <span data-ttu-id="13900-5377">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5377">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5379">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5379">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5380">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5381">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5382">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5383">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5384">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5386">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5386">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5387">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5387">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5388">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5388">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5389">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5389">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5390">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5390">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5391">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5391">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5392">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5392">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5393">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5393">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5394">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5394">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5395">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5395">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5396">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5396">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5397">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5397">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5398">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5398">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5399">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5399">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5400">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5400">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5401">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5401">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5402">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5402">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5403">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5403">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5404">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5404">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5405">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5405">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5406">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5406">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5407">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5407">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5408">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5408">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5409">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5409">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5410">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5410">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5411">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5411">CPU Lockable</span></span> | \- |
| <span data-ttu-id="13900-5412">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5412">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5413">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5413">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5414">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5414">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5415">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5415">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5416">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5416">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5417">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5417">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5418">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5418">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5419">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5419">Video Decoder Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5421">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5421">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5423">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5423">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5425">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5425">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5426">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5426">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="13900-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="13900-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="13900-5428">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5428">Target</span></span> | <span data-ttu-id="13900-5429">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5429">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5430">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5430">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5431">16</span><span class="sxs-lookup"><span data-stu-id="13900-5431">16</span></span> |
| <span data-ttu-id="13900-5432">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5432">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5434">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5434">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5435">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5435">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5436">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5436">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5437">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5437">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5438">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5438">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5439">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5439">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5441">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5441">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5442">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5442">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5443">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5443">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5444">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5444">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5445">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5445">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5446">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5446">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5447">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5447">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5448">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5448">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5449">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5449">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5450">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5450">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5451">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5451">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5452">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5452">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5453">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5454">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5455">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5456">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5457">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5457">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5458">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5459">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5460">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5461">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5462">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5462">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5463">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5464">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5465">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5466">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5466">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5468">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5468">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5469">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5469">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5470">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5470">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5471">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5471">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5472">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5472">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5473">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5474">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5474">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5475">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5475">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5477">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5477">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5479">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5479">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5481">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5481">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5482">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5482">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="13900-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="13900-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="13900-5484">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5484">Target</span></span> | <span data-ttu-id="13900-5485">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5485">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5486">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5486">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5487">32</span><span class="sxs-lookup"><span data-stu-id="13900-5487">32</span></span> |
| <span data-ttu-id="13900-5488">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5488">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5490">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5490">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5491">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5491">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5492">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5493">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5494">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5495">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5495">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5497">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5497">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5498">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5498">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5499">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5499">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5500">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5500">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5501">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5501">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5502">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5502">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5503">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5503">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5504">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5504">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5505">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5505">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5506">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5506">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5507">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5507">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5508">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5508">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5509">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5509">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5510">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5510">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5511">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5511">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5512">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5512">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5513">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5513">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5514">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5514">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5515">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5515">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5516">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5516">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5517">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5517">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5518">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5518">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5519">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5519">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5520">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5520">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5521">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5521">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5522">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5522">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5524">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5524">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5525">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5525">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5526">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5526">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5527">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5527">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5528">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5528">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5529">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5529">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5530">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5530">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5531">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5531">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5533">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5533">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5535">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5535">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5537">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5537">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5538">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5538">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="13900-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="13900-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="13900-5540">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5540">Target</span></span> | <span data-ttu-id="13900-5541">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5541">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5542">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5542">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5543">32</span><span class="sxs-lookup"><span data-stu-id="13900-5543">32</span></span> |
| <span data-ttu-id="13900-5544">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5544">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5546">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5546">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5547">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5548">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5549">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5550">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5551">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5553">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5553">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5554">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5554">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5555">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5555">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5556">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5556">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5557">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5558">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5559">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5559">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5560">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5561">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5561">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5562">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5563">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5564">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5564">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5565">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5565">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5566">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5566">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5567">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5567">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5568">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5568">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5569">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5569">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5570">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5570">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5571">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5571">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5572">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5572">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5573">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5573">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5574">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5574">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5575">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5575">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5576">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5576">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5577">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5577">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5578">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5578">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5580">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5581">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5582">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5583">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5584">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5584">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5585">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5586">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5587">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5587">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5589">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5589">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5591">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5591">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5593">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5593">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5594">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="13900-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="13900-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="13900-5596">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5596">Target</span></span> | <span data-ttu-id="13900-5597">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5597">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5598">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5599">8</span><span class="sxs-lookup"><span data-stu-id="13900-5599">8</span></span> |
| <span data-ttu-id="13900-5600">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5600">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5602">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5602">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5603">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5604">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5605">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5606">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5607">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5609">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5610">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5611">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5612">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5613">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5614">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5615">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5615">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5616">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5617">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5617">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5618">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5619">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5620">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5621">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5622">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5622">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5623">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5623">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5624">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5624">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5625">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5625">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5626">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5626">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5627">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5627">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5628">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5628">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5629">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5629">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5630">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5630">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5631">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5631">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5632">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5632">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5633">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5633">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5634">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5634">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5636">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5636">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5637">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5637">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5638">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5638">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5639">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5639">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5640">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5640">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5641">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5641">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5642">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5642">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5643">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5643">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5645">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5645">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5647">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5647">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5649">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5649">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5650">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="13900-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="13900-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="13900-5652">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5652">Target</span></span> | <span data-ttu-id="13900-5653">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5653">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5654">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5655">8</span><span class="sxs-lookup"><span data-stu-id="13900-5655">8</span></span> |
| <span data-ttu-id="13900-5656">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5656">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5658">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5658">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5659">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5659">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5660">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5660">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5661">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5661">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5662">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5662">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5663">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5663">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5665">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5665">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5666">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5666">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5667">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5667">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5668">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5668">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5669">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5669">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5670">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5670">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5671">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5671">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5672">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5672">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5673">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5673">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5674">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5674">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5675">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5676">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5676">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5677">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5678">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5679">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5680">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5681">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5681">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5682">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5683">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5684">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5685">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5686">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5687">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5688">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5689">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5690">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5690">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5692">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5693">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5694">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5695">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5696">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5696">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5697">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5698">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5699">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-5700">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5700">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5702">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5702">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-5703">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5703">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5704">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5704">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="13900-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="13900-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="13900-5706">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5706">Target</span></span> | <span data-ttu-id="13900-5707">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5707">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5708">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5708">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5709">8</span><span class="sxs-lookup"><span data-stu-id="13900-5709">8</span></span> |
| <span data-ttu-id="13900-5710">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5710">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5712">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5712">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5713">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5713">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5714">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5714">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5715">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5715">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5716">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5716">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5717">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5717">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5719">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5719">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5720">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5721">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5721">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5722">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5722">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5723">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5723">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5724">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5724">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5725">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5725">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5726">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5726">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5727">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5727">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5728">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5729">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5730">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5731">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5732">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5733">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5734">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5735">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5735">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5736">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5737">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5738">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5739">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5740">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5740">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5741">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5742">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5743">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5744">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5744">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5746">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5747">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5748">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5749">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5750">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5750">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5751">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5752">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5752">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5753">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5753">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-5754">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5754">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5756">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-5757">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5757">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5758">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="13900-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="13900-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="13900-5760">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5760">Target</span></span> | <span data-ttu-id="13900-5761">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5761">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5762">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5763">8</span><span class="sxs-lookup"><span data-stu-id="13900-5763">8</span></span> |
| <span data-ttu-id="13900-5764">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5764">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5766">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5766">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5767">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5768">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5769">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5770">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5771">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5771">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5773">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5773">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5774">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5774">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5775">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5775">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5776">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5776">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5777">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5777">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5778">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5778">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5779">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5779">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5780">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5780">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5781">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5781">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5782">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5783">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5784">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5784">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5785">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5785">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5786">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5786">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5787">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5787">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5788">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5788">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5789">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5789">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5790">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5790">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5791">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5791">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5792">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5792">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5793">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5793">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5794">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5794">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5795">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5795">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5796">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5796">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5797">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5797">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5798">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5798">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5800">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5801">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5802">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5803">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5804">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5804">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5805">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5806">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5807">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-5808">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5808">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5810">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5810">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-5811">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5811">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5812">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5812">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="13900-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="13900-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="13900-5814">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5814">Target</span></span> | <span data-ttu-id="13900-5815">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5815">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5816">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5816">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5817">16</span><span class="sxs-lookup"><span data-stu-id="13900-5817">16</span></span> |
| <span data-ttu-id="13900-5818">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5818">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="13900-5820">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5820">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5821">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5821">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5822">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5822">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5823">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5823">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5824">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5824">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5825">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5827">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5828">TextureCube</span></span> | \- |
| <span data-ttu-id="13900-5829">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5829">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="13900-5830">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5830">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="13900-5831">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5831">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5832">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5832">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5833">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5833">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5834">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5834">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5835">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5835">Mipmap</span></span> | \- |
| <span data-ttu-id="13900-5836">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5836">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5837">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5837">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5838">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5838">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5839">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5839">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5840">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5840">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5841">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5841">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5842">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5842">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5843">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5843">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5844">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5844">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5845">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5845">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5846">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5846">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5847">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5847">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5848">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5848">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5849">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5849">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5850">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5850">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5851">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5851">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5852">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5852">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5854">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5854">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5855">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5855">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5856">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5856">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5857">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5857">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5858">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5858">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5859">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5859">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5860">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5860">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5861">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5861">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-5862">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5862">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5864">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5864">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-5865">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5865">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5866">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5866">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="13900-5867">DXGI_FORMAT_B4G4R4A4 \_ unorm<sup></sup> -Fehler (115)</span><span class="sxs-lookup"><span data-stu-id="13900-5867">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="13900-5868">Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5868">Target</span></span> | <span data-ttu-id="13900-5869">Support</span><span class="sxs-lookup"><span data-stu-id="13900-5869">Support</span></span> |
| - | - |
| <span data-ttu-id="13900-5870">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="13900-5870">Bits Per Element (BPE)</span></span> | <span data-ttu-id="13900-5871">16</span><span class="sxs-lookup"><span data-stu-id="13900-5871">16</span></span> |
| <span data-ttu-id="13900-5872">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="13900-5872">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5874">Buffer</span><span class="sxs-lookup"><span data-stu-id="13900-5874">Buffer</span></span> | \- |
| <span data-ttu-id="13900-5875">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="13900-5875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="13900-5876">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="13900-5876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="13900-5877">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="13900-5877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="13900-5878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="13900-5878">Texture1D</span></span> | \- |
| <span data-ttu-id="13900-5879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="13900-5879">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5881">Texture3D</span><span class="sxs-lookup"><span data-stu-id="13900-5881">Texture3D</span></span> | \- |
| <span data-ttu-id="13900-5882">TextureCube</span><span class="sxs-lookup"><span data-stu-id="13900-5882">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5884">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="13900-5884">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5886">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5886">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5888">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5888">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="13900-5889">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="13900-5889">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="13900-5890">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="13900-5890">Shader gather4</span></span> | \- |
| <span data-ttu-id="13900-5891">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="13900-5891">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="13900-5892">MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5892">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5894">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="13900-5894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="13900-5895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5895">RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5896">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5897">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="13900-5897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="13900-5898">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="13900-5898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="13900-5899">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5900">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="13900-5900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="13900-5901">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="13900-5901">Typed UAV</span></span> | \- |
| <span data-ttu-id="13900-5902">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="13900-5902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="13900-5903">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="13900-5904">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="13900-5904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="13900-5905">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="13900-5905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="13900-5906">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="13900-5906">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="13900-5907">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="13900-5907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="13900-5908">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="13900-5908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5909">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="13900-5909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="13900-5910">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="13900-5910">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="13900-5912">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5913">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="13900-5913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="13900-5914">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="13900-5914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="13900-5915">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="13900-5915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="13900-5916">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="13900-5916">Multisample Load</span></span> | \- |
| <span data-ttu-id="13900-5917">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="13900-5917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="13900-5918">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="13900-5918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="13900-5919">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="13900-5919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="13900-5920">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5920">Video Processor Input</span></span> | \- |
| <span data-ttu-id="13900-5921">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="13900-5921">Video Processor Output</span></span> | \- |
| <span data-ttu-id="13900-5922">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5922">Shared Resource</span></span> | \- |
| <span data-ttu-id="13900-5923">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="13900-5923">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="13900-5924">Notizen formatieren</span><span class="sxs-lookup"><span data-stu-id="13900-5924">Format notes</span></span>

<span data-ttu-id="13900-5925">Der Zweck des-Formats kann sich von einer Hardware Funktionsebene zur nächsten ändern.</span><span class="sxs-lookup"><span data-stu-id="13900-5925">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="13900-5926"><sup>L</sup> : typloses Format</span><span class="sxs-lookup"><span data-stu-id="13900-5926"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="13900-5927"><sup>PCs</sup> : teilweise typisiertes, castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="13900-5927"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="13900-5928"><sup>FCS</sup> : vollständig typisiertes, castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="13900-5928"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="13900-5929"><sup>FNS</sup> : vollständig typisiertes, nicht-castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="13900-5929"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="13900-5930"><sup>PCC</sup> : teilweise typisiertes, castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="13900-5930"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="13900-5931"><sup>FCC</sup> : vollständig typisiertes, castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="13900-5931"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="13900-5932"><sup>FNC</sup> : vollständig typisiertes, nicht-castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="13900-5932"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="13900-5933"><sup>V</sup> : Videoformat</span><span class="sxs-lookup"><span data-stu-id="13900-5933"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="13900-5934">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="13900-5934">Related topics</span></span>

[<span data-ttu-id="13900-5935">D3D12-Hardware Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="13900-5935">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="13900-5936">[Implementieren von Schatten Puffern für Direct3D Feature Level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="13900-5936">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="13900-5937">Mapping von Legacy Formaten</span><span class="sxs-lookup"><span data-stu-id="13900-5937">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="13900-5938">Programmier Handbuch für DXGI</span><span class="sxs-lookup"><span data-stu-id="13900-5938">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
